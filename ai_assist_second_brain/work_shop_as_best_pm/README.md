# Workshops

**Направляемые рабочие сессии, которые завершаются готовым артефактом**

Промпты здесь запускают модерируемую многошаговую сессию — вопросы по принципу
Generative Guidance, контрольные точки (checkpoint gates), рекомендации с учётом
контекста — и создают сам **артефакт**: battle card, PRD, opportunity solution
tree, бизнес-кейс, canvas.

Каждый воркшоп следует паттерну Generative Guidance v2 (см.
[`generative-guidance-pattern.md`](../generative-guidance-pattern.md))
или чекпоинтной совместной работе (см.
[`interaction-modes.md`](../interaction-modes.md)).

## Что доступно

| Workshop | Что создаёт | Фреймворк |
|----------|-------------|-----------|
| **[battle-card-workshop.md](battle-card-workshop.md)** | Конкурентная battle card | Критерий material shift; артефакт для полевых действий |
| **[prd-workshop.md](prd-workshop.md)** | Полный PRD, раздел за разделом | Шаблон вашей команды (или канонический запасной вариант); контрольные точки |
| **[opportunity-solution-tree-workshop.md](opportunity-solution-tree-workshop.md)** | Opportunity solution tree + первый эксперимент | Continuous discovery Терезы Торрес |
| **[feature-investment-workshop.md](feature-investment-workshop.md)** | Бизнес-кейс build / don't-build | Путь к выручке, структура затрат, ROI с поправкой на маржу |
| **[problem-framing-canvas-workshop.md](problem-framing-canvas-workshop.md)** | Постановка проблемы + вопрос «How might we» | MITRE ITK Problem Framing Canvas |
| **[painstorming-workshop.md](painstorming-workshop.md)** | Таблица PAINstorming | MITRE ITK: Persona, Activities, Insights, Needs |
| **[lean-ux-canvas-workshop.md](lean-ux-canvas-workshop.md)** | Заполненный Lean UX Canvas + эксперимент с минимальной работой | Gothelf Lean UX Canvas v2 |
| **[product-sunset-workshop.md](product-sunset-workshop.md)** | Полный план EOL продукта/фичи, раздел за разделом | Шаблон вашей команды (или канонический запасной вариант из 6 разделов); работает в паре с промптом анонса EOL |

У многих воркшопов есть «прямой» шаблон-близнец в `/prompts/` для сессий,
где контекст уже загружен, — смотрите строку `Companion:` в каждом файле.
