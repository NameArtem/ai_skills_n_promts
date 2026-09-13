# Market Intelligence

**Автономные исследовательские промпты: ИИ делает полевую работу, вы
проверяете данные**

Промпты в этой директории следуют режиму взаимодействия **autonomous
investigation** (см. [`interaction-modes.md`](../interaction-modes.md)).
Там, где `/prompts/` предполагает, что контекст держите вы, а
`/prompt-generators/` вытягивает его из вас, исследования направляют ИИ
на мир: веб-поиск, опубликованные данные, достоверные источники — с
цитатами, помеченными выводами и значениями по умолчанию, которые
позволяют промпту работать без вас.

Последнее свойство важно: поскольку эти промпты действуют по
наилучшим доступным данным, когда никто не отвечает на вопросы, они
подходят для агентов, циклов и запусков по расписанию — конкурентное
сканирование, обновляемое ежеквартально, рыночный снимок, который
диффится против прошлого месяца.

## Контракт, который соблюдает каждое исследование

- **Question budget** — жёсткий лимит (обычно 3), затем продолжение с
  помеченными допущениями
- **Search plan gate** — план из 3 пунктов, показываемый перед
  исследованием; он продолжается, если вы его не измените
- **Evidence labels** — каждая ключевая точка помечена **Fact**
  (поддержано источником), **Inference** (интерпретация на основе
  данных) или **Assumption** (рабочая догадка)
- **Реальные, проверяемые URL** — и список «не выдумывать», называющий
  конкретные риски фабрикации в данной области
- **Just Enough Mode по умолчанию** — самые сильные находки, короткие
  пункты; Verbose только по запросу
- **Стабильная схема вывода** — чтобы запуск N и запуск N+1 были
  сравнимы, а это то, что делает возможными повторные запуски по
  расписанию и отчёты о дельтах
- **Блок Final Step** — ровно 4 пронумерованных следующих варианта

## Начните здесь, если у вас есть компания и приглашение в календаре

**[full-spectrum-company-sweep-prompt.md](full-spectrum-company-sweep-prompt.md)**
прогоняет все семь дисциплин сбора подряд по одной компании, сводит их
правилом укладки уверенности и завершается брифингом, готовым к звонку:
резюме на шестьдесят секунд, три вещи, которые стоит сказать, вопросы,
которые вам зададут, с ответами, и утверждения, которые нельзя делать.
Один промпт, один прогон, без оркестрации.

Используйте его, когда компания внезапно становится важной, а у вас есть
одна сессия, чтобы разобраться. Всё ниже даёт больше глубины по более
узкому вопросу — берите эти промпты, когда этот обход скажет, какой
канал тонкий.

## Что доступно

| Промпт | Лучше всего для |
|--------|----------|
| **[full-spectrum-company-sweep-prompt.md](full-spectrum-company-sweep-prompt.md)** | Всё об одной компании за один прогон: все семь дисциплин, сведённые, с финальным брифингом, готовым к звонку |
| **[competitive-research-snapshot-prompt.md](competitive-research-snapshot-prompt.md)** | Just-enough исследование конкурентного ландшафта с цитируемыми снимками, матрицей сравнения и выводами «so what» |
| **[competitive-intel-watch-prompt.md](competitive-intel-watch-prompt.md)** | Плановый мониторинг дельт против предыдущего снимка: только материальные сдвиги, с флагами обновлений battle card |
| **[market-landscape-scan-prompt.md](market-landscape-scan-prompt.md)** | Картирование сегментов рынка, игроков, субститутов и белого пространства до оценки размера или позиционирования |
| **[voice-of-customer-miner-prompt.md](voice-of-customer-miner-prompt.md)** | Добыча отзывов, app store и форумов ради неудовлетворённых потребностей и слабостей конкурентов, с цитируемыми данными |
| **[earnings-executive-signal-refresh-prompt.md](earnings-executive-signal-refresh-prompt.md)** | Ежеквартальный дифф исполнительских и стратегических сигналов одной компании против предыдущего профиля |
| **[pricing-packaging-tracker-prompt.md](pricing-packaging-tracker-prompt.md)** | Отслеживание цен и пакетов конкурента как дифференцируемого временного ряда |
| **[pestel-delta-monitor-prompt.md](pestel-delta-monitor-prompt.md)** | Ежеквартальное пересканирование макро-факторов: что двинулось, что сломалось, что вошло в кадр |
| **[tam-sam-som-analysis-prompt.md](tam-sam-som-analysis-prompt.md)** | Оценка размера рынка с цитатами, снизу вверх, с чувствительностью best/base/worst |
| **[battle-card-builder-prompt.md](battle-card-builder-prompt.md)** | Battle card с цитируемыми данными из публичных источников: метки на каждое утверждение, формат полевых действий |
| **[swot-analysis-prompt.md](swot-analysis-prompt.md)** | SWOT с источниками, дисциплиной квадрантов и пересечениями S-O / W-T |
| **[porters-five-forces-prompt.md](porters-five-forces-prompt.md)** | Чтение структуры отрасли: пять оценённых сил с документированными сигналами, следствие для пула прибыли |
| **[ansoff-matrix-prompt.md](ansoff-matrix-prompt.md)** | Варианты роста с данными по каждому квадранту, с соблюдением градиента риска, рекомендуемая последовательность |
| **[all-source-fusion-prompt.md](all-source-fusion-prompt.md)** | Ситуационная комната: сводит сигналы других исследований в истории с оценкой уверенности и ответами, сопоставленными с артефактами |

### Сборочный этаж (один обход на дисциплину)

Семь дисциплинарных обходов, по одному на дисциплину сбора из
компендиума, каждый со встроенными источниками дисциплины и цепочками
сигнал → вывод. Все семь выпускают **одну и ту же готовую к фьюжну схему
Signal Inventory**, так что любая комбинация стыкуется в
[all-source-fusion-prompt.md](all-source-fusion-prompt.md), а запуск N
диффится против запуска N-1 по расписанию (см.
[loops/fusion-cadence-routine.md](../loops/fusion-cadence-routine.md)
для управляемого ритма).

| Промпт | Дисциплина | Основные источники питания |
|--------|------------|---------------|
| **[osint-collection-prompt.md](osint-collection-prompt.md)** | Open Source: пресса, аналитики, соцсети, отзывы, конференции, предсказательные рынки | Battle cards, позиционирование |
| **[finint-collection-prompt.md](finint-collection-prompt.md)** | Financial: отчётности, уклончивость на earnings, закупки, регистрации, суверенный капитал | Battle cards, capture rates SOM |
| **[geoint-demoint-collection-prompt.md](geoint-demoint-collection-prompt.md)** | Geospatial and demographic: количество предприятий, профессии, зарплаты, торговые потоки | TAM/SAM/SOM, ICP, personas, messaging |
| **[techint-collection-prompt.md](techint-collection-prompt.md)** | Technical: патенты, товарные знаки, технографика, changelog-и, стандарты, препринты | Ставки на дорожную карту |
| **[humint-collection-prompt.md](humint-collection-prompt.md)** | Human: всплески найма, ходы талантов, настроения, фрейминг win/loss | Ставки на дорожную карту, battle cards |
| **[sigint-collection-prompt.md](sigint-collection-prompt.md)** | Signals: веб/ценовые диффы, SEO/SEM, SSL-сертификаты, метаданные app store | Battle cards, ценовая стратегия |
| **[masint-collection-prompt.md](masint-collection-prompt.md)** | Measurement and signature: цепочка поставок, объекты, операционный «выхлоп», сертификации | Оценка угроз, прогноз запусков |

## Полка ремесла

Промпты выше — исполняемый слой. Доктрина за ними — что собирать, где и
какие цепочки сигнал → вывод прогонять — живёт в [`reference/`](reference/):

- **[competitive-research-compendium.md](reference/competitive-research-compendium.md)**
  — восемь дисциплин сбора разведывательного сообщества (OSINT,
  FININT, GEOINT/DEMOINT, TECHINT, HUMINT, SIGINT, MASINT, All-Source
  Fusion), сопоставленные с артефактами PM, с источниками, цепочками
  сигналов, укладкой уверенности и каденцией фьюжна
- **[regional-source-overlays-eu-mena.md](reference/regional-source-overlays-eu-mena.md)**
  — региональные оверлеи источников ЕС и MENA: закупочные платформы,
  реестры, статистические бюро и региональные guardrails (дисциплины не
  меняются между рынками; меняются источники и бремя доказательств)

Файлы в `reference/` — это доктрина, а не промпты: у них нет блока
комментариев, и они исключены из каталога и валидатора.

### Покрытие дисциплин

Как промпты этой директории ложатся на дисциплины компендиума. У каждой
дисциплины теперь есть выделенный обход сбора; вторая колонка называет
промпты глубоких погружений, которым каждый обход передаёт работу:

| Дисциплина | Обход сбора | Глубокие погружения |
|---|---|---|
| OSINT | osint-collection | market-landscape-scan, competitive-research-snapshot, voice-of-customer-miner |
| FININT | finint-collection | earnings-executive-signal-refresh |
| GEOINT/DEMOINT | geoint-demoint-collection | tam-sam-som-analysis, pestel-delta-monitor |
| TECHINT | techint-collection | — |
| HUMINT | humint-collection | [prompts/win-loss-analysis](../prompts/win-loss-analysis-prompt.md) (синтезирует интервью вашей команды в ground truth) |
| SIGINT | sigint-collection | competitive-intel-watch, pricing-packaging-tracker |
| MASINT | masint-collection | — (аномалии разграничиваются через FININT и HUMINT) |
| All-Source Fusion | all-source-fusion | swot-analysis, porters-five-forces, ansoff-matrix, а battle-card-builder потребляет сведённые данные |

## Как система собирается вместе

Три слоя, одно движение — или
[full-spectrum-company-sweep-prompt.md](full-spectrum-company-sweep-prompt.md),
который проходит все три внутренне для одной компании, когда у вас нет
времени оркестрировать.

1. **Collect** — инстанцируйте вовлечение (шесть переменных компендиума:
   TARGET, MARKET, GEOGRAPHY, BUYER, CAPABILITY, DECISION), затем
   запустите обходы сбора для значимых дисциплин. Новый рынок?
   Начните шире: landscape scan → снимок игроков → затем обход.
2. **Fuse** — когда 2+ дисциплины держат сигналы, запустите **all-source
   fusion**: тест независимости, укладка уверенности, копание в
   конфликтах. Интервью win/loss вашей команды
   ([prompts/win-loss-analysis-prompt.md](../prompts/win-loss-analysis-prompt.md))
   — это ground truth, подтверждающая или опровергающая то, что вывели
   публичные сигналы.
3. **Act** — действенные истории обновляют артефакты: **five forces**
   читает структуру отрасли, **SWOT** — позицию одного игрока, **Ansoff** —
   варианты роста, **TAM/SAM/SOM** — размер, а **battle-card builder**
   вооружает поле. Затем настройте ритм с
   [loops/fusion-cadence-routine.md](../loops/fusion-cadence-routine.md).

**Рабочий пример — запуск, замеченный до пресс-релиза:** ваш еженедельный
обход SIGINT находит новый SSL-сертификат для
`analytics.competitor.com` (подготовка запуска, за недели вперёд). Это
флагует TECHINT, который находит кластер из 8 патентных заявок в
классификациях аналитики плюс две статьи на arXiv от их сотрудников.
TECHINT флагует свою пару для фьюжна, HUMINT, которая находит 25
вакансий по дата-инжинирингу за квартал против базовых 4. Фьюжн
укладывает: три независимые дисциплины, одна история — действенно.
Earnings-проход FININT добавляет CFO, уклоняющегося от вопроса о
капитальных расходах на аналитику (намерение, подтверждённое деньгами).
Ответ до их запуска: ход зрелости в battle card, решение по дорожной
карте «ускоряться/уступать». Ваш следующий раунд win/loss подтверждает,
решает ли аналитика сделки на самом деле, — и реестр питает следующий
фьюжн-запуск.

Чтобы построить кастомное исследование, используйте
[prompt-generators/research-agent-prompt-generator.md](../prompt-generators/research-agent-prompt-generator.md).
Чтобы превратить любой вывод отсюда в историю для стейкхолдеров, используйте
[storytelling/Generator - Research-to-Narrative Bridge.md](../storytelling/Generator%20-%20Research-to-Narrative%20Bridge.md).
Для рецептов циклов, пакетов и рутин поверх этих промптов смотрите
[loops/](../loops/) — swot-batch, market-sizing-loop и
competitive-watch-routine прогоняют фреймворки этой директории под
управляемым повторением, а **fusion-cadence-routine** гоняет весь
сборочный этаж по еженедельному / ежемесячному / ежеквартальному /
ежегодному ритму компендиума.