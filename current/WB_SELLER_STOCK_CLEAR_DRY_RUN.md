# WB_SELLER_STOCK_CLEAR_DRY_RUN
_Автогенерировано 2026-04-20T19:35:24. Ничего не отправлено в WB API._

## What would happen

- Method: **PUT /api/v3/stocks/{warehouseId}** with `amount: 0`
- DELETE inventory used: **NO**
- Total rows: 0
- Eligible rows (execution_allowed): 0
- Total units that would be zeroed: 0

## Per Warehouse

| Warehouse ID | Name | Eligible rows | Units |
|---|---|---|---|

## Top 50 SKU by current_amount

| Warehouse | SKU | Supplier Article | Current amount | Execution allowed |
|---|---|---|---|---|

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
