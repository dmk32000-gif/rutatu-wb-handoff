# Manual FBO Supply Creation Instructions

## Статус
Автоматическое создание FBO поставки через WB API невозможно.
Причина: marketplace-api.wildberries.ru/api/v3/supplies — FBS endpoint (создаёт WB-GI-* бандлы).
FBO/FBW поставки создаются только вручную в seller.wildberries.ru.

## Неверные поставки (DO NOT USE)
- WB-GI-232254686 — FBS bundle, WRONG_TYPE_DO_NOT_USE
- WB-GI-232323720 — FBS bundle, WRONG_TYPE_DO_NOT_USE

## Почему неверно
Обе поставки созданы через FBS /api/v3/supplies endpoint.
WB-GI-* prefix = FBS (Fulfillment by Seller, со склада продавца).
Нужен тип FBO (Fulfillment by WB, на склад WB). Это разные склады и разные поставки.

## Что нужно сделать

### Шаг 1. Открыть seller.wildberries.ru
URL: https://seller.wildberries.ru

### Шаг 2. Создать поставку
Путь: Поставки → FBW → Склад WB → Создать поставку

Параметры:
- Склад: Электросталь
- Тип упаковки: Короб
- Количество коробов: 1

### Шаг 3. Добавить товары в поставку
Добавить следующие nmId и количества:

| nmId | Количество |
|---|---|
| 46051603 | 95 |
| 19398868 | 25 |
| 20958317 | 26 |
| 19398867 | 28 |
| 154978092 | 1 |
| 12793460 | 5 |
| 13875583 | 36 |
| 13875570 | 19 |
| 12793454 | 18 |
| 55212491 | 17 |
| 25647921 | 4 |
| 15842151 | 2 |
| 16078759 | 1 |
| 21028560 | 3 |
| 14601649 | 2 |

Итого: 15 SKU / 282 шт.

### Шаг 4. Получить Supply ID
После создания WB выдаст числовой ID поставки (формат: 38XXXXXXX или 46XXXXXXX).
Это НЕ WB-GI-* — это числовой ID FBO поставки.

### Шаг 5. Зарегистрировать в агенте
```
.venv\Scripts\python.exe -m app.cli wb register-supply <числовой_id>
```

## Текущее состояние агента
current_state: WRONG_SUPPLY_TYPE_PENDING_MANUAL_FBO_CREATE
fbo_supply_id: null
fox2box_handover_allowed: false
label_workflow_allowed: false (ждём числовой FBO supply ID)

generated_at: 2026-04-21T04:38:14Z
