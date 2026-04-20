# P&L Source Matrix

_Сгенерировано автоматически. Дата: 2026-04-20._
_Основан на результатах WB_API_ACCESS_AUDIT.md._

## Матрица источников по компонентам P&L

| component | source | api_or_file | available_now | confidence | daily_estimated | monthly_closed | missing_what |
|---|---|---|---|---|---|---|---|
| revenue | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| commission | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| logistics | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| storage | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| acceptance | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| returns | WB reportDetailByPeriod | API (WB_API_TOKEN_ANALYTICS) | YES | real | yes | yes | — |
| ads | WB Advertising API | API (WB_API_TOKEN_ADS) | NO | missing | no | no | Токен WB_API_TOKEN_ADS не задан |
| tax | Расчётный (УСН 6%/15%) | calculated | ESTIMATED | estimated | yes (estimate) | yes (estimate) | Уточнить режим налогообложения |
| cogs | data/input/cogs.csv | file | NO | missing | no | no | Файл cogs.csv отсутствует; себестоимость нужно заполнить вручную |
| net_profit | Все выше | derived | PARTIAL | estimated | partial | partial | ads + cogs недоступны → чистая прибыль неполная |

## Детали по компонентам

### Доступны сейчас (через WB_API_TOKEN_ANALYTICS)
- **revenue** — строки с `supplierReward` / `ppvzForPay` из reportDetailByPeriod
- **commission** — `commission_percent` × `retail_amount` из отчёта
- **logistics** — `delivery_rub` из отчёта
- **storage** — `storage_fee` из отчёта
- **acceptance** — `penalty` / `deduction` строки
- **returns** — строки с `return` в `doc_type_name`

### Требуют дополнительных токенов
- **ads** — нужен `WB_API_TOKEN_ADS` или `WB_API_TOKEN_MARKETING`. Без этого реклама = 0 в P&L, что завышает прибыль.

### Требуют ручного ввода (никогда не в API)
- **cogs** — себестоимость производства. WB не знает ваши производственные затраты. Нужен файл `data/input/cogs.csv`.
- **tax** — зависит от режима налогообложения (УСН 6%, УСН 15%, ОСНО). Можно оценить, но не получить из API.

## Итог готовности P&L

```
Выручка          ████████ 100% (API готов)
Комиссия         ████████ 100% (API готов)
Логистика        ████████ 100% (API готов)
Хранение         ████████ 100% (API готов)
Приёмка          ████████ 100% (API готов)
Возвраты         ████████ 100% (API готов)
Реклама          ░░░░░░░░   0% (токен отсутствует)
Налог            ████░░░░  50% (оценочно)
Себестоимость    ░░░░░░░░   0% (файл отсутствует)
Чистая прибыль   ████░░░░  ~60% (без ads и COGS)
```

## Что нужно сделать

1. **Получить WB_API_TOKEN_ADS** — обратиться в WB кабинет поставщика → Настройки → Доступ к API → Реклама
2. **Заполнить `data/input/cogs.csv`** — себестоимость каждого SKU (производство + материалы + труд)
3. **Уточнить налоговый режим** у Ксении/бухгалтера — УСН 6% от выручки или 15% от прибыли
