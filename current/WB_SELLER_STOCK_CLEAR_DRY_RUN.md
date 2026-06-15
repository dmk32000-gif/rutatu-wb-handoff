# WB_SELLER_STOCK_CLEAR_DRY_RUN
_Автогенерировано 2026-04-21T11:47:46. Ничего не отправлено в WB API._

## What would happen

- Method: **PUT /api/v3/stocks/{warehouseId}** with `amount: 0`
- DELETE inventory used: **NO**
- Total rows: 1
- Eligible rows (execution_allowed): 1
- Total units that would be zeroed: 18

## Per Warehouse

| Warehouse ID | Name | Eligible rows | Units |
|---|---|---|---|
| 135327 | Мой склад | 1 | 18 |

## Top 50 SKU by current_amount

| Warehouse | SKU | Supplier Article | Current amount | Execution allowed |
|---|---|---|---|---|
| Мой склад | 4680134964742 | 505-12х16-japanese | 18 | True |

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
