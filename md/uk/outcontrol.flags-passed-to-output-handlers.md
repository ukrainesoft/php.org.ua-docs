---
navigation:
  - outcontrol.working-with-output-handlers.md: « Робота з оброблювачами висновку
  - outcontrol.output-handler-return-values.md: 'Значення оброблювача виводу, що повертаються »'
  - index.md: PHP Manual
  - outcontrol.user-level-output-buffers.md: Буфери виводу користувача
title: 'Прапори, що передаються обробникам виводу'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Прапори, що передаються обробникам виводу

Бітова маска, передана у другий параметр `phase` обробника виводу дає інформацію про виклик обробника.

> **Зауваження**: До бітової маски можна включати більше одного прапора, а для перевірки того, чи встановлено прапор, вказують побітовий оператор. `&`

**Увага**

Значение флага\*\*`PHP_OUTPUT_HANDLER_WRITE`**и его псевдонима**`PHP_OUTPUT_HANDLER_CONT`\*\* одно , тому чи встановлено воно, визначають лише операторами рівності [equality operator](language.operators.comparison.md) `==`или`===`

PHP встановлює такі прапори на конкретному етапі життєвого циклу оброблювача: **`PHP_OUTPUT_HANDLER_START`** - при першому виклику оброблювача . **`PHP_OUTPUT_HANDLER_FINAL`**или его псевдоним**`PHP_OUTPUT_HANDLER_END`** - При останньому викликі оброблювача, тобто він відключається. PHP також установить цей прапор, коли буфери вимикаються процесом завершення роботи PHP.

Конкретний виклик обробника встановлює такі прапори: **`PHP_OUTPUT_HANDLER_FLUSH`** - при запуску обробника викликом функції [ob\_flush()](function.ob-flush.md). . **`PHP_OUTPUT_HANDLER_WRITE`**или его псевдоним**`PHP_OUTPUT_HANDLER_CONT`** — коли розмір вмісту дорівнює або перевищує розмір буфера, а обробник викликаний під час автоматичного очищення буфера . **`PHP_OUTPUT_HANDLER_FLUSH`** - коли обробник запущено викликом функцій [ob\_clean()](function.ob-clean.md) [ob\_end\_clean()](function.ob-end-clean.md) або [ob\_get\_clean()](function.ob-get-clean.md). При виклику функцій [ob\_end\_clean()](function.ob-end-clean.md) або [ob\_get\_clean()](function.ob-get-clean.md)он также устанавливает флаг\*\*`PHP_OUTPUT_HANDLER_FINAL`\*\*

> **Зауваження**: Під час виклику функцій [ob\_end\_flush()](function.ob-end-flush.md) або [ob\_get\_flush()](function.ob-get-flush.md), флаг\*\*`PHP_OUTPUT_HANDLER_FINAL`**будет установлен, а флаг**`PHP_OUTPUT_HANDLER_FLUSH`\*\* - Ні.
