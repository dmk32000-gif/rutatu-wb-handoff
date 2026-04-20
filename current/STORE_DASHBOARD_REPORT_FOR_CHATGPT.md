# STORE_DASHBOARD_REPORT_FOR_CHATGPT
_Автогенерировано 2026-04-20T16:57. Передавать в ChatGPT вместо zip._

---

## Dashboard pages

| Страница | URL | Статус |
|---|---|---|
| Обзор магазина | /overview | ✅ |
| P&L | /profit | ✅ |
| Артикулы | /skus | ✅ |
| Досорт | /restock | ✅ |
| Качество данных | /data-quality | ✅ |
| Действия | /actions | ✅ |

---

## Profit Engine Status

| Компонент | Статус | Детали |
|---|---|---|
| Finance API (reportDetailByPeriod) | ✅ Доступен | WB_API_TOKEN_ANALYTICS задан и валиден |
| Ads API (реклама) | ✅ Доступен | WB_API_TOKEN_ADS задан |
| COGS файл | ❌ Отсутствует | data/input/cogs.csv не заполнен |
| Закрытый P&L (месячный) | ❌ Недоступен | Нужен Finance API + cogs.csv |
| Оценочный дневной P&L | ✅ Доступен | Finance API подключён |
| Placeholder экономика осталось | 170 SKU | Нужно обновить unit_economics.csv |

---

## WB API Access Summary

| Токен | Присутствует | Покрывает |
|---|---|---|
| WB_API_TOKEN_ANALYTICS | SET | Statistics API: продажи, остатки, заказы, возвраты, reportDetailByPeriod |
| WB_API_TOKEN_FBW | SET | Marketplace API: поставки, цены, тарифы |
| WB_API_TOKEN_ADS | SET | Advertising API: расходы на рекламу |
| WB_API_TOKEN_FINANCE | EMPTY (не задан) | Finance/Documents API: реестры выплат, акты |

### HTTP-проверки (последний аудит)

| Endpoint | Статус |
|---|---|
| statistics-api .../stocks | 200 OK |
| statistics-api .../reportDetailByPeriod | 200 OK |
| suppliers-api .../supplies | URLError (сетевая проблема) |

---

## P&L Source Matrix Summary

| Компонент | Доступен сейчас | Источник | Что отсутствует |
|---|---|---|---|
| revenue | да | reportDetailByPeriod | — |
| commission | да | reportDetailByPeriod | — |
| logistics | да | reportDetailByPeriod | — |
| storage | да | reportDetailByPeriod | — |
| acceptance | да | reportDetailByPeriod | — |
| returns | да | reportDetailByPeriod | — |
| ads | да | Advertising API | — |
| tax | оценочно | расчётный | уточнить налоговый режим |
| cogs | нет | data/input/cogs.csv | заполнить cogs.csv вручную |
| net_profit | частично | производное | ads + cogs |

---

## Unit Economics Completion Summary

- Всего placeholder SKU (значение = 50.0): **170**
- can_be_replaced_via_api: **yes** (reportDetailByPeriod содержит комиссию и логистику по SKU)
- requires_cogs_manual: **yes** — себестоимость никогда не приходит из WB API, нужен ручной ввод
- Полный план: см. data/output/current/UNIT_ECONOMICS_COMPLETION_PLAN.md

---

## Что пользователь должен предоставить следующим

### Токены WB API (по категориям — без значений)
- Все необходимые токены уже заданы ✅

### Локальные файлы
- **data/input/cogs.csv** — Себестоимость по каждому SKU (производство + материалы + труд). Шаблон: data/input/cogs_template.csv

### Действия в дашборде (видны на /actions и /data-quality)

- ❌ Заполнить data/input/cogs.csv → разблокирует расчёт чистой прибыли
- ⚠️ Обновить unit_economics.csv: 170 SKU с placeholder 50 ₽

---

## Обзор магазина (Store Overview)

| Параметр | Значение |
|---|---|
| Активных SKU | 285 |
| Прибыльных SKU (реальная экономика) | 60 |
| Убыточных SKU | 55 |
| Placeholder экономика (50 ₽) | 170 |
| Нет профиля упаковки | 0 |
| Нет тарифа | 2 |
| Кандидаты на досорт (при партии) | 49 |
| Блокеры качества данных | 0 |
| Производство активно | Да |
| Статус черновика | PRODUCTION_IN_PROGRESS |

---

## Текущий черновик досорта

| Параметр | Значение |
|---|---|
| Статус | PRODUCTION_IN_PROGRESS |
| Склад | Электросталь |
| SKU | 15 |
| Единиц | 282 шт |
| Коробок | 1 |
| Производство готово | 2026-04-21 |
| Заказ отправлен | 2026-04-19 |

---

## Топ-10 прибыльных SKU

| # | Артикул | Прибыль/шт | Упаковка |
|---|---|---|---|
| 1 | 471-10х48-lotus | 164.90 ₽ | tube_63x170 |
| 2 | RUTATUslv375-16x48-rose | 147.70 ₽ | tube_63x170 |
| 3 | RUTATUslv192-16x48-mehendi | 136.68 ₽ | tube_63x170 |
| 4 | 148-24x32-magnolia | 132.56 ₽ | tube_63x235 |
| 5 | RUTATUslv217-16x48-flowers | 126.78 ₽ | tube_63x170 |
| 6 | RUTATUGAR269-10x48-lotus-ornament | 126.72 ₽ | tube_63x170 |
| 7 | RUTATUslv364-16x48-dragon | 125.62 ₽ | tube_63x170 |
| 8 | 498-16x48-flowers-and-berries | 120.19 ₽ | tube_63x170 |
| 9 | 150-24x32-rose | 118.46 ₽ | tube_63x235 |
| 10 | 082-16x48-peonies | 114.94 ₽ | tube_63x170 |

---

## Топ-10 проблем качества данных

| Артикул | Тип проблемы | Серьёзность | Описание |
|---|---|---|---|

---

## Доска действий

| Артикул | Действие | Причина | Риск | Статус |
|---|---|---|---|---|
| 471-10х48-lotus | В производстве | Активное производство | low | in_progress |
| RUTATUslv375-16x48-rose | В производстве | Активное производство | low | in_progress |
| RUTATUslv192-16x48-mehendi | В производстве | Активное производство | low | in_progress |
| 148-24x32-magnolia | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| RUTATUslv217-16x48-flowers | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| RUTATUGAR269-10x48-lotus-ornament | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| RUTATUslv364-16x48-dragon | В производстве | Активное производство | low | in_progress |
| 498-16x48-flowers-and-berries | В производстве | Активное производство | low | in_progress |
| 150-24x32-rose | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 082-16x48-peonies | В производстве | Активное производство | low | in_progress |
| 341-16x48-fairy | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 132-16x48-pattern | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 080-24x32-peonies | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| RUTATUslv361-16x48-skull | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 357-16x48-snake | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 292-16x48-zmeya-tsveti | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 219-24x16-uzor-pod-grud | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 338-16x48-sleeve | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| RUTATUhip161-24x32-dragon | Досортить при партии | Транспорт >5% | low | waiting_for_batch |
| 508-24х32-flowers | Досортить при партии | Транспорт >5% | low | waiting_for_batch |

---

## Что нужно для полного P&L

- WB_API_TOKEN_ADS (расходы на рекламу по кампаниям и SKU)
- data/input/cogs.csv — себестоимость производства по каждому SKU
- Обновлённые unit_economics.csv (сейчас 170 SKU с placeholder 50 ₽)
- Уточнить налоговый режим (УСН 6% / 15% / ОСНО)

---

## Источники данных

Загружены: unit_economics.csv, sku_packaging_map.csv, wb_whitelist_active.csv, reports/restock_plan.csv, RUN_STATUS.md, audit_log.jsonl
