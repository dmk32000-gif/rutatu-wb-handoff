# DATA_TRUTH_RECONCILIATION
_Автогенерировано 2026-04-20T17:04. Dashboard v1.1 canonical metrics._

---

## Canonical Metric Counts

| Метрика | canonical_value |
|---|---|
| total_sku | 285 |
| real_positive_economics_count | 60 |
| real_negative_economics_count | 55 |
| zero_economics_count | 0 |
| placeholder_50_count | 170 |
| missing_economics_count | 0 |
| invalid_economics_count | 0 |
| packaging_explicit_count | 243 |
| packaging_size_fallback_count | 36 |
| packaging_default_tattoo_count | 6 |
| packaging_missing_count | 0 |
| hard_blocker_count | 0 |
| warning_count | 257 |

---

## Packaging Classification Breakdown

| Source | Count | Meaning |
|---|---|---|
| explicit_map | 243 | Profile explicitly set in sku_packaging_map.csv |
| size_fallback | 36 | Inferred from size code (10x48→tube_170, 16x48→tube_170, 24x32→tube_235) |
| default_tattoo_packet | 6 | No tube-size match → tattoo_packet (business rule) |
| missing | 0 | Explicit profile present but INVALID (hard blocker) |

---

## Economics Classification Breakdown

| Status | Count | Meaning |
|---|---|---|
| real_positive | 60 | Profit > 0, not placeholder |
| real_negative | 55 | Profit < 0 (warning) |
| zero | 0 | Profit == 0 |
| placeholder_50 | 170 | Value == 50.0 (stub, unreliable) |
| missing | 0 | No economics data (hard blocker) |
| invalid | 0 | Invalid value (hard blocker) |

---

## Metric Consistency (all pages vs canonical)

| Page | Metric | canonical_value | Status |
|---|---|---|---|
| /overview | profitable_sku_count | 60 | OK |
| /overview | negative_profit_sku_count | 55 | OK |
| /overview | placeholder_economics_count | 170 | OK |
| /overview | no_packaging_count | 0 | OK |
| /overview | hard_blocker_count | 0 | OK |
| /profit | real_positive_count | 60 | OK |
| /profit | real_negative_count | 55 | OK |
| /skus | packaging_profile_from_classifier | canonical | OK |
| /data-quality | no_false_no_packaging_profile | fixed | OK |
| /actions | packaging_classification | canonical | OK |

---

## False Blocker Fix (v1.1)

Before v1.1, SKUs with blank `packaging_profile` in sku_packaging_map.csv
were flagged as `no_packaging_profile` blockers even when their size code
or SKU name contained a recognized tube size (10x48, 16x48, 24x32).

After v1.1, `classify_packaging_profile()` applies size fallback and
defaults unknown sizes to `tattoo_packet` — so no SKU ever gets
`PackagingSource.missing` unless an explicit but INVALID profile is set.

| SKU | Size in name | Resolved profile | Source | Was false blocker? |
|---|---|---|---|---|
| 148-24x32-magnolia | in SKU name | tube_63x235 | size_fallback | YES → fixed |
| 471-10х48-lotus | in SKU name | tube_63x170 | size_fallback | YES → fixed |
| 498-16x48-flowers-and-berries | in SKU name | tube_63x170 | size_fallback | YES → fixed |

---

## Data Sources

Loaded: unit_economics.csv, sku_packaging_map.csv, wb_whitelist_active.csv, reports/restock_plan.csv, RUN_STATUS.md, audit_log.jsonl
