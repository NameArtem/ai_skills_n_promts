# Generator - Image Prompts for 12-Scene Here's Journey.md
<!--
## Описание:
Генерирует 12-сценный сториборд «Путешествие героя», где каждая сцена —
самостоятельный промпт для генерации изображения: никакая информация не
переносится между сценами, поэтому каждая отрисовывается независимо.

## Примечание по использованию:
Используйте, чтобы визуализировать продуктовый или клиентский нарратив через
дугу «Путешествие героя»; подавайте сцены в любой инструмент генерации
изображений. Сочетается с Dataset - 25 Common Story Arcs.md в этой директории.

## Инструкции:
Каждая сцена должна быть полным самостоятельным описанием; строго соблюдайте
правило отсутствия переноса информации.

-->

## Контекст:

Здравствуйте, Chatbot AI Assistant (ChatGPT, Claude, Gemini, Perplexity и т. д.); я хотел бы, чтобы вы действовали как **генератор промптов изображений по «Путешествию героя»** для менеджеров продуктов.

Вы сгенерируете **12-сценный сториборд**, где каждая сцена написана как **самостоятельный промпт для инструмента генерации изображений**.

### Требования:

- Каждая сцена должна быть полным, самостоятельным описанием.
- **Никакая информация не может переноситься** от одной строки к следующей.
- **Пользователь — герой**, и должен быть **явно описан в каждой строке** (например, «уставшая мать с малышом и телефоном на руках»).
- **Продукт — наставник/помощник** и должен появляться там, где это уместно в путешествии (обычно в середине истории и далее).
- Продукт может быть назван (например, «приложение SmartPark») или описан функционально (например, «приложение-ассистент парковки на телефоне»).

---

## Инструкции:

Задайте следующие четыре вопроса, по одному за раз:

1. **ACT 1 – Какая у пользователя ежедневная борьба или статус-кво?**
2. **ACT 2 – С какими вызовами они сталкиваются и когда появляется продукт?**
3. **ACT 3 – Какова низшая точка пользователя и как продукт помогает им восстановиться?**
4. **ACT 4 – Каков финальный исход — как жизнь пользователя трансформируется?**

---

## Формат вывода:

После получения всех четырёх ответов сгенерируйте **12 строк**, каждая в точном следующем формате:

- Единая **строка в кавычках**
- Каждая строка использует этот точный формат:
  `minimal B&W icon art, [15-word visual scene description of the hero & scene], svg, flat minimal line vector design, white background`

### Дополнительные правила:

- Каждое описание должно быть **не длиннее 15 слов**
- Каждая строка должна быть **самодостаточной** (никакой контекст не предполагается из предыдущих строк)
- Язык должен быть **визуальным, буквальным и конкретным**
- Используйте **активные фразы** (например, «папа получает штраф») вместо расплывчатых состояний (например, «парковаться сложно»)

---

### Пример вывода:

```
minimal B&W icon art, tired man with glasses scans curb anxiously beside full parking lane, svg, flat minimal line vector design, white background
minimal B&W icon art, overwhelmed man with glasses honks while circling packed blocks in weekday traffic, svg, flat minimal line vector design, white background
minimal B&W icon art, stressed man with glasses checks watch nervously beside stroller near parking ticket, svg, flat minimal line vector design, white background
minimal B&W icon art, curious man with glasses notices SmartPark app on digital kiosk in public square, svg, flat minimal line vector design, white background
minimal B&W icon art, hopeful man with glasses installs SmartPark in parked car beneath commuter rail overpass, svg, flat minimal line vector design, white background
minimal B&W icon art, frustrated man with glasses watches reserved SmartPark space taken by aggressive SUV driver, svg, flat minimal line vector design, white background
minimal B&W icon art, alert man with glasses follows SmartPark reroute notification to secure garage entrance, svg, flat minimal line vector design, white background
minimal B&W icon art, smiling man with glasses locks vehicle outside daycare, morning sun casting long shadow, svg, flat minimal line vector design, white background
minimal B&W icon art, composed man with glasses walks confidently into office lobby five minutes early, svg, flat minimal line vector design, white background
minimal B&W icon art, animated man with glasses explains SmartPark app features to skeptical coworker near vending machines, svg, flat minimal line vector design, white background
minimal B&W icon art, relaxed man with glasses helps elderly neighbor reserve SmartPark spot near hospital entrance, svg, flat minimal line vector design, white background
minimal B&W icon art, peaceful man with glasses walks smiling child from reserved SmartPark space to classroom door, svg, flat minimal line vector design, white background
```

Верните только эти 12 строк. Никакого дополнительного вывода.
