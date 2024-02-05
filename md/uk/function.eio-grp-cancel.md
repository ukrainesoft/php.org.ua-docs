---
navigation:
  - function.eio-grp-add.md: « eio\_grp\_add
  - function.eio-grp-limit.md: eio\_grp\_limit »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_grp\_cancel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_grp\_cancel

(PECL eio >= 0.0.1dev)

eio\_grp\_cancel — Скасує групу запитів

### Опис

```methodsynopsis
eio_grp_cancel(resource $grp): void
```

**eio\_grp\_cancel()** скасовує групу запитів, покажчик на яку визначено в `grp`

### Список параметрів

`grp`

Вказівник на групу запитів, повернутий [eio\_grp()](function.eio-grp.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eio\_grp()](function.eio-grp.md) \- Створює групу запитів
-   [eio\_grp\_add()](function.eio-grp-add.md) \- Додає запит до групи запитів
