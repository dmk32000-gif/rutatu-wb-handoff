# WB API Access Audit

_Сгенерировано автоматически. Дата: 2026-04-20._

> Токены проверены только по наличию (SET/EMPTY). Значения нигде не выводятся.

## Токены в .env

| Переменная | Присутствует |
|---|---|
| WB_API_TOKEN_ANALYTICS | SET |
| WB_API_TOKEN_FBW | SET |
| WB_API_TOKEN_FINANCE | EMPTY (не задан) |
| WB_API_TOKEN_ADS | EMPTY (не задан) |
| WB_API_TOKEN_MARKETING | EMPTY (не задан) |

## Результаты HTTP-проверок

| source_name | endpoint | required_token | token_present | http_status | available | reason | needed_for |
|---|---|---|---|---|---|---|---|
| Statistics/stocks | https://statistics-api.wildberries.ru/api/v1/supplier/stocks?dateFrom=2026-01-01 | WB_API_TOKEN_ANALYTICS | true | 200 | yes | OK | Остатки на складе WB по дням |
| Statistics/reportDetailByPeriod | https://statistics-api.wildberries.ru/api/v5/supplier/reportDetailByPeriod?dateFrom=2026-04-01&dateTo=2026-04-20 | WB_API_TOKEN_ANALYTICS | true | 200 | yes | OK | Финансовый отчёт: выручка, комиссия, логистика, хранение по SKU |
| Supplies/FBW | https://suppliers-api.wildberries.ru/api/v3/supplies?limit=1 | WB_API_TOKEN_FBW | true | none | no | URLError (network/DNS) | Поставки FBO: создание, статус, отправка |

## Выводы по категориям

### WB_API_TOKEN_ANALYTICS
- Покрывает: Statistics API — продажи, остатки, заказы, возвраты, reportDetailByPeriod
- Статус: **VALID** (HTTP 200 на обоих тестовых endpoints)
- Позволяет получить: выручку, комиссию WB, логистику, хранение, возвраты — по SKU и по дням

### WB_API_TOKEN_FBW
- Покрывает: Marketplace/Suppliers API — поставки, цены, тарифы
- Статус: **UNDETERMINED** — токен SET, но запрос вернул URLError (сетевая проблема или DNS с данного хоста)
- Требует проверки из другой сети или напрямую с VPS

### WB_API_TOKEN_FINANCE (отсутствует)
- Нужен для: Finance/Documents API — реестры выплат, акты сверки, финансовые документы
- Статус: **MISSING** — не задан в .env
- Что упускаем: точные суммы выплат WB (после всех вычетов), официальные финансовые документы

### WB_API_TOKEN_ADS / WB_API_TOKEN_MARKETING (отсутствуют)
- Нужны для: Advertising API — расходы на рекламу по кампаниям и SKU
- Статус: **MISSING** — не заданы в .env
- Что упускаем: расходы на рекламу (ads spend) в P&L

## Компоненты P&L vs доступность токенов

| Компонент P&L | Источник | Токен | Доступен сейчас |
|---|---|---|---|
| Выручка (revenue) | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Комиссия WB | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Логистика | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Хранение (storage) | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Приёмка (acceptance) | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Возвраты | reportDetailByPeriod | WB_API_TOKEN_ANALYTICS | ДА |
| Реклама (ads) | Advertising API | WB_API_TOKEN_ADS | НЕТ |
| Налог | расчётный (УСН 6% / 15%) | — | ОЦЕНОЧНО |
| Себестоимость (COGS) | data/input/cogs.csv | локальный файл | НЕТ (файл отсутствует) |
| Чистая прибыль | всё выше | — | ЧАСТИЧНО |
