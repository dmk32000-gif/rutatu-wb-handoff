# WB_SELLER_STOCK_CLEAR_PREFLIGHT
_Автогенерировано 2026-04-21T05:58:05._

## Summary

- Marketplace token available: ✅ Yes
- Seller warehouses found: 1
- SKU with FBS stock > 0: 0
- Total units on seller warehouse: 0
- Plan rows (to zero): 0

## Seller Warehouses

| ID | Name | SKU with stock | Units | Query status |
|---|---|---|---|---|
| 135327 | Мой склад | 0 | 0 | ok |

## Safety

- DELETE inventory: **NOT used** — strategy is `update_amount_zero`
- FBO/WB warehouse stocks: **NOT touched** — only seller warehouse (FBS) stocks
- Execute requires: `WB_SELLER_STOCK_CLEAR_ENABLED=true` + `WB_SELLER_STOCK_CLEAR_MODE=execute` + `WB_SELLER_STOCK_CLEAR_EXECUTE_ACK=true`

## Next steps

```bash
python -m app.cli wb-seller-stock clear --mode dry-run
# Review WB_SELLER_STOCK_CLEAR_DRY_RUN.md
# Then set gates and execute:
python -m app.cli wb-seller-stock clear --mode execute
```
