# WB_SELLER_STOCK_CLEAR_DRY_RUN
_Автогенерировано 2026-04-20T16:57:07. Ничего не отправлено в WB API._

## What would happen

- Method: **PUT /api/v3/stocks/{warehouseId}** with `amount: 0`
- DELETE inventory used: **NO**
- Total rows: 62
- Eligible rows (execution_allowed): 62
- Total units that would be zeroed: 1347

## Per Warehouse

| Warehouse ID | Name | Eligible rows | Units |
|---|---|---|---|
| 135327 | Мой склад | 62 | 1347 |

## Top 50 SKU by current_amount

| Warehouse | SKU | Supplier Article | Current amount | Execution allowed |
|---|---|---|---|---|
| Мой склад | RUTATUNBT079 | 079-17x5-romashki | 44 | True |
| Мой склад | RUTATUNBT301 | 301-6x16-gold | 43 | True |
| Мой склад | 4680134964773 | 508-24х32-flowers | 41 | True |
| Мой склад | RUTATUNBT303 | 303-6x16-nature | 40 | True |
| Мой склад | 4680134964537 | 219-24x16-uzor-pod-grud | 38 | True |
| Мой склад | RUTATUNBT155 | 155-17x5-gold-silver | 35 | True |
| Мой склад | 4680134964766 | 507-12х32-flowers-tenderness | 34 | True |
| Мой склад | RUTATUNBT110 | 110-16x24-lotus | 33 | True |
| Мой склад | RUTATUEAS209 | RUTATUeas209-12x16-flower | 32 | True |
| Мой склад | RUTATUEAS235 | 235-12x16-lotus | 32 | True |
| Мой склад | RUTATUNBT263 | 263-16x24-dragon | 32 | True |
| Мой склад | RUTATUcht376 | RUTATU376-16x24-lotos | 31 | True |
| Мой склад | RUTATUSML222 | RUTATUSML222-6x8-snake | 31 | True |
| Мой склад | RUTATUNBT106 | 106-12x16-meh-lotus | 29 | True |
| Мой склад | 4680134964339 | 298-8x24-drakoni | 28 | True |
| Мой склад | RUTATUslv192 | RUTATUslv192-16x48-mehendi | 28 | True |
| Мой склад | RUTATUani362 | RUTATUani362-12x16-bear | 27 | True |
| Мой склад | RUTATUNBT154 | 154-17x5-silver | 27 | True |
| Мой склад | RUTATUNBT153 | 153-17x5-stars | 26 | True |
| Мой склад | RUTATUORN206 | RUTATUorn206-8x24-floral | 26 | True |
| Мой склад | 4680134961741 | 272-16x48-flowers | 25 | True |
| Мой склад | 4680134963882 | 444-16x24-dragon | 25 | True |
| Мой склад | 4680134963998 | 334-6х16-pero | 25 | True |
| Мой склад | RUTATUNBT138 | 138-17х5-pink | 25 | True |
| Мой склад | RUTATUNBT057 | 057-6x8-footbal | 24 | True |
| Мой склад | RUTATUNBT143 | 143-12x16-braslet-pion | 24 | True |
| Мой склад | RUTATUSLV217 | RUTATUslv217-16x48-flowers | 24 | True |
| Мой склад | RUTATUNBT123 | 123-17x5-silver | 23 | True |
| Мой склад | RUTATUNBT076 | 076-17x5-nature | 21 | True |
| Мой склад | RUTATUNBT122 | 122-17x5-gold | 21 | True |
| Мой склад | RUTATUNBT145 | 145-16x24-peones | 21 | True |
| Мой склад | RUTATUNBT274 | 274-6x16-snake | 21 | True |
| Мой склад | 4680134963509 | 043-16x48-japanese | 20 | True |
| Мой склад | RUTATUMEH194 | RUTATUmeh194-16x24-cherep | 20 | True |
| Мой склад | RUTATUNBT124 | 124-10x48-branch-berries | 20 | True |
| Мой склад | RUTATUNBT135 | RUTATUNBT135-8x24-rose | 20 | True |
| Мой склад | RUTATUNBT302 | 302-6x16-silver | 20 | True |
| Мой склад | 4680134961772 | RUTATUhnd275-6x16-dragon | 19 | True |
| Мой склад | RUTATUNBT139 | 139-17x5-green | 19 | True |
| Мой склад | 4680134960478 | RUTATUbut241-8x24-dragon | 18 | True |
| Мой склад | 4680134963738 | 399-12x16-tsveti | 18 | True |
| Мой склад | RUTATUNBT338 | 338-16x48-sleeve | 18 | True |
| Мой склад | RUTATUPLS221 | RUTATUPLS221-12x16-paporotnik | 18 | True |
| Мой склад | RUTATUNBT148 | 148-24x32-magnolia | 17 | True |
| Мой склад | 4680134964827 | 514-17х5-hearts | 16 | True |
| Мой склад | 4680134960904 | RUTATUCHST265-24x32-boho | 15 | True |
| Мой склад | 4680134964728 | 501-12х16-snake-eagle | 14 | True |
| Мой склад | 4680134964797 | 510-16x48-flowers | 14 | True |
| Мой склад | 4680134964926 | 339-16x48-lily. | 14 | True |
| Мой склад | RUTATUFRL224 | RUTATUFRL224-17x5-babochki | 13 | True |

## Execute readiness

To execute, set all three flags in `.env`:
```
WB_SELLER_STOCK_CLEAR_ENABLED=true
WB_SELLER_STOCK_CLEAR_MODE=execute
WB_SELLER_STOCK_CLEAR_EXECUTE_ACK=true
```

Then run:
```bash
python -m app.cli wb-seller-stock clear --mode execute
```

> WARNING: execute will send real PUT requests to WB API. Review dry-run output first.
