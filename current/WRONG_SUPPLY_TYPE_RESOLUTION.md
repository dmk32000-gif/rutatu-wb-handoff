# Wrong Supply Type — Resolution Guide

## Проблема

Поставка `WB-GI-232323720` создана как **FBS** (по ID с префиксом `WB-GI-`).

FBS-поставки предназначены для отправки со склада продавца (FBS = Fulfillment by Seller).
Для пополнения FBO-склада Wildberries нужна поставка с `deliveryType=fbo`.

## Последствия использования FBS-поставки

- ШК короба (FBW box labels) **недоступны** через API `/api/v3/supplies/{id}/barcode`
- ШК поставки (supply barcode) **недоступен** через API
- Передача Fox2Box **заблокирована** — Fox2Box принимает только FBO-поставки
- Поставка не появится в разделе FBO-склада WB

## Шаги для устранения

### 1. Сгенерировать новую FBO-поставку (dry-run — только посмотреть)

```
python -m app.cli wb recreate-current-supply --mode dry-run
```

Это создаст:
- `data/output/current/recreate_fbo_supply_payload.json` — payload для новой поставки
- `data/output/current/RECREATE_FBO_SUPPLY_DRY_RUN.md` — отчёт и инструкция

### 2. Проверить payload в RECREATE_FBO_SUPPLY_DRY_RUN.md

Убедиться:
- `deliveryType: fbo`
- Все SKU и количества сохранены
- Нет лишних позиций

### 3. Выполнить создание новой поставки (только после явного GO)

```
python -m app.cli wb recreate-current-supply --mode execute
```

**ВНИМАНИЕ: не запускать без явного подтверждения от Дмитрия/Ксении.**

### 4. После успешного создания новой поставки

- Запустить: `python -m app.cli wb-labels audit`
- Получить ШК короба и ШК поставки из нового supply ID
- Продолжить label workflow

## Статус

detected_at: 2026-04-21T04:09:06Z
original_supply_id: WB-GI-232323720
original_type: FBS
action_required: RECREATE_WITH_FBO_TYPE
