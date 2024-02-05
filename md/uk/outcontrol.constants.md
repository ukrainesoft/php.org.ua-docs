---
navigation:
  - outcontrol.resources.md: « Типи ресурсів
  - outcontrol.output-buffering.md: Буферизація висновку »
  - index.md: PHP Manual
  - book.outcontrol.md: Контроль виведення
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**Прапори стану, що передаються обробнику виведення**

Наступні прапори передаються як частина бітової маски на другий параметр (`phase`) оброблювача виведення, встановленого функцією [ob\_start()](function.ob-start.md) :

**`PHP_OUTPUT_HANDLER_START`**(int)

Вказує, що буферизація виведення розпочалася.

**`PHP_OUTPUT_HANDLER_WRITE`**(int)

Вказує, що буфер виводу очищається і є дані для виведення.

**`PHP_OUTPUT_HANDLER_FLUSH`**(int)

Означає, що буфер був скинутий (очищений та виведений).

**`PHP_OUTPUT_HANDLER_CLEAN`**(int)

Це означає, що буфер був очищений.

**`PHP_OUTPUT_HANDLER_FINAL`**(int)

Це означає, що це остання операція буферизації.

**`PHP_OUTPUT_HANDLER_CONT`**(int)

Буфер був очищений, але буферизація виводу буде продовжена.

Це синонім для **`PHP_OUTPUT_HANDLER_WRITE`**

**`PHP_OUTPUT_HANDLER_END`**(int)

Означає, що буферизація виводу завершена.

Це синонім для **`PHP_OUTPUT_HANDLER_FINAL`**

**Прапори керування буфером виводу**

Наступні прапори передають у вигляді бітової маски у третій параметр (`flags`) оброблювача виведення, встановленого функцією [ob\_start()](function.ob-start.md) :

**`PHP_OUTPUT_HANDLER_CLEANABLE`**(int)

Визначає, чи буфер виводу, створений функцією [ob\_start()](function.ob-start.md), бути очищений функцією [ob\_clean()](function.ob-clean.md). Це прапор не управляє поведінкою функцій [ob\_end\_clean()](function.ob-end-clean.md) або [ob\_get\_clean()](function.ob-get-clean.md)

**`PHP_OUTPUT_HANDLER_FLUSHABLE`**(int)

Визначає, чи буфер виводу, створений функцією [ob\_start()](function.ob-start.md), бути скинуто (виведено та очищено) функцією [ob\_flush()](function.ob-flush.md). Це прапор не управляє поведінкою функцій [ob\_end\_flush()](function.ob-end-flush.md) або [ob\_get\_flush()](function.ob-get-flush.md)

**`PHP_OUTPUT_HANDLER_REMOVABLE`**(int)

Визначає, чи буфер виводу, створений функцією [ob\_start()](function.ob-start.md), бути видалено до завершення скрипту або під час виклику функцій [ob\_end\_clean()](function.ob-end-clean.md) [ob\_end\_flush()](function.ob-end-flush.md) [ob\_get\_clean()](function.ob-get-clean.md) або [ob\_get\_flush()](function.ob-get-flush.md)

**`PHP_OUTPUT_HANDLER_STDFLAGS`**(int)

Значення за промовчанням для прапорів буфера виводу. Рівняється **`PHP_OUTPUT_HANDLER_CLEANABLE`** **`PHP_OUTPUT_HANDLER_FLUSHABLE`** **`PHP_OUTPUT_HANDLER_REMOVABLE`**

**Прапори статусу оброблювача виводу**

Наступні прапори – частина бітової маски ключа `flags` масиву, що повертається функцією [ob\_get\_status()](function.ob-get-status.md) :

**`PHP_OUTPUT_HANDLER_STARTED`**(int)

Це означає, що був викликаний обробник висновку.

**`PHP_OUTPUT_HANDLER_DISABLED`**(int)

Вказує, що обробник виводу вимкнено. Цей прапор буде встановлено, коли обробник виводу поверне **`false`**, завершується з помилкою при обробці буфера або його було встановлено до виклику обробника виведення.

**`PHP_OUTPUT_HANDLER_PROCESSED`**(int)

Вказує, що обробник виведення успішно обробив буфер.
