---
navigation:
  - outcontrol.resources.md: « Типи ресурсів
  - outcontrol.examples.md: Приклади »
  - index.md: PHP Manual
  - book.outcontrol.md: Контроль виведення
title: Обумовлені константи
---
# Обумовлені константи

Наведені нижче константи завжди доступні як частина ядра PHP.

**`PHP_OUTPUT_HANDLER_START`** (int)

Служить ознакою те, що буферування висновку почалося.

**`PHP_OUTPUT_HANDLER_WRITE`** (int)

Служить ознакою те, що буфер виводу очищається й у ньому перебувають дані висновку.

**`PHP_OUTPUT_HANDLER_FLUSH`** (int)

Позначає, що буфер був скинутий (очищений та виведений).

**`PHP_OUTPUT_HANDLER_CLEAN`** (int)

Позначає, що буфер було очищено.

**`PHP_OUTPUT_HANDLER_FINAL`** (int)

Це означає, що це остання операція буферування.

**`PHP_OUTPUT_HANDLER_CONT`** (int)

Буфер був очищений, але буферування виводу буде продовжено.

Це синонім для **`PHP_OUTPUT_HANDLER_WRITE`**

**`PHP_OUTPUT_HANDLER_END`** (int)

Позначає, що буферування виводу завершено.

Це синонім для **`PHP_OUTPUT_HANDLER_FINAL`**

**`PHP_OUTPUT_HANDLER_CLEANABLE`** (int)

Визначає чи буфер виводу, створений [проstart()](function.ob-start.md)бути очищеним.

**`PHP_OUTPUT_HANDLER_FLUSHABLE`** (int)

Визначає чи буфер виводу, створений [проstart()](function.ob-start.md), бути скинутий (виведений та очищений).

**`PHP_OUTPUT_HANDLER_REMOVABLE`** (int)

Визначає чи буфер виводу, створений [проstart()](function.ob-start.md), бути вилученим до завершення скрипта.

**`PHP_OUTPUT_HANDLER_STDFLAGS`** (int)

Значення за промовчанням для прапорів буфера виводу. Рівняється **`PHP_OUTPUT_HANDLER_CLEANABLE`** **`PHP_OUTPUT_HANDLER_FLUSHABLE`** **`PHP_OUTPUT_HANDLER_REMOVABLE`**
