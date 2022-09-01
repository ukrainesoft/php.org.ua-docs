---
navigation:
  - function.eio-grp-add.html: « eiogrpadd
  - function.eio-grp-limit.html: eiogrplimit »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiogrpcancel
---
# eiogrpcancel

(PECL eio >= 0.0.1dev)

eiogrpcancel — Скасує групу запитів

### Опис

```methodsynopsis
eio_grp_cancel(resource $grp): void
```

**eiogrpcancel()** скасовує групу запитів, покажчик на яку визначено в `grp`

### Список параметрів

`grp`

Вказівник на групу запитів, повернутий [eiogrp()](function.eio-grp.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eiogrp()](function.eio-grp.md) - Створює групу запитів
-   [eiogrpadd()](function.eio-grp-add.md) - Додає запит до групи запитів
