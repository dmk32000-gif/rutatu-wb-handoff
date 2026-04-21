# Recreate FBO Supply — Dry Run

## Текущая поставка (НЕВЕРНЫЙ ТИП)

supply_id: WB-GI-232254686
type: FBS
name: RUTATU Электросталь 1box 2026-04-19

## Новый FBO payload (preview)

```json
{
  "name": "RUTATU Электросталь 1box 2026-04-19_FBO_RECREATE",
  "deliveryType": "fbo",
  "items_count": 15,
  "items_preview": [
  {
    "nmId": 46051603,
    "quantity": 95
  },
  {
    "nmId": 19398868,
    "quantity": 25
  },
  {
    "nmId": 20958317,
    "quantity": 26
  },
  {
    "nmId": 19398867,
    "quantity": 28
  },
  {
    "nmId": 154978092,
    "quantity": 1
  }
]
  ... and 10 more items
}
```

Полный payload записан в: `data/output/current/recreate_fbo_supply_payload.json`

## Команда для выполнения (только с явным GO)

```
python -m app.cli wb recreate-current-supply --mode execute
```

## WARNING

⚠️ **НЕ ЗАПУСКАТЬ** без явного подтверждения от Дмитрия/Ксении.

Команда `--mode execute` создаст новую поставку в WB через API и обновит состояние агента.
Это действие нельзя автоматически отменить.

## Dry-run сгенерирован

generated_at: 2026-04-21T03:41:38Z
mode: dry-run
action_blocked: true (waiting for explicit GO)
