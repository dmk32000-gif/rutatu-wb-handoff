# RUTATU WB Agent — ChatGPT Handoff

_Last updated: 2026-04-20T17:50:52_

---

## Current State

| Параметр | Значение |
|---|---|
| Active model | production_backed |
| Dashboard version | v1.1 |
| Production status | PRODUCTION_IN_PROGRESS |
| Active draft | Электросталь |
| Production due | 2026-04-21 |
| Total SKU | 285 |

### Current blockers

- ❌ data/input/cogs.csv не заполнен — чистая прибыль не рассчитывается
- ❌ 170 SKU с placeholder экономикой (50 ₽)

### Next action

Статус производства: **PRODUCTION_IN_PROGRESS**.
Следующая отгрузка: **2026-04-21**.

---

## Files

| Файл | Статус | Описание |
|---|---|---|
| INDEX.md | — | Этот файл — главная точка входа |
| CURRENT_STATE.json | ✅ | Машинно-читаемое состояние |
| STORE_DASHBOARD_REPORT_FOR_CHATGPT.md | ✅ | Полный отчёт по магазину |
| DASHBOARD_SUMMARY_FOR_CHATGPT.md | ✅ | Краткий обзор + Profit Engine |
| ACTION_BOARD_FOR_CHATGPT.md | ✅ | Доска действий по SKU |
| RESTOCK_CURRENT_FOR_CHATGPT.md | ✅ | Текущий досорт + кандидаты |
| DATA_QUALITY_FOR_CHATGPT.md | ✅ | Блокеры и предупреждения |
| DATA_TRUTH_RECONCILIATION.md | ✅ | Сверка метрик по источникам |
| WB_API_ACCESS_AUDIT.md | ✅ | Аудит доступности API |
| P_AND_L_SOURCE_MATRIX.md | ✅ | Матрица источников P&L |
| UNIT_ECONOMICS_COMPLETION_PLAN.md | ✅ | План замены placeholder экономики |
| RUN_STATUS.md | ✅ | Статус последнего запуска агента |
| HANDOFF_MANIFEST.json | — | Манифест пакета с контрольными суммами |

---

## Executive Summary

| Метрика | Значение |
|---|---|
| Всего SKU | 285 |
| Прибыльных SKU (реальная экономика) | 60 |
| Убыточных SKU | 55 |
| Placeholder экономика (50 ₽) | 170 |
| Missing экономика | 0 |
| Нет упаковки | 0 |
| Блокеры качества | 0 |
| Предупреждений | 227 |
| Досорт черновик | PRODUCTION_IN_PROGRESS |
| Производственный заказ | Активен |
| FBS seller warehouse stock | zero ✅ |
| Last FBS clear | 62 rows / 0 units / verified zero |

---

## What ChatGPT Should Analyze Next

1. Проверить статус производства и дату готовности
2. Сверить кандидатов на следующий досорт с RESTOCK_CURRENT_FOR_CHATGPT.md
3. Оценить распределение прибыльных/убыточных SKU в STORE_DASHBOARD_REPORT_FOR_CHATGPT.md
4. Проверить данные по P&L в P_AND_L_SOURCE_MATRIX.md
5. Заполнить unit economics для 170 SKU — см. UNIT_ECONOMICS_COMPLETION_PLAN.md
6. Заполнить data/input/cogs.csv для расчёта чистой прибыли

---

## Safety Note

> Этот handoff не содержит секретов, токенов, `.env` или сырых API-ответов.
> Все данные — read-only аналитика.
> Проверено: `scripts/validate_chatgpt_handoff_safety.py`

