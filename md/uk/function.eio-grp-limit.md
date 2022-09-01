---
navigation:
  - function.eio-grp-cancel.html: « eiogrpcancel
  - function.eio-grp.html: eiogrp »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiogrplimit
---
# eiogrplimit

(PECL eio >= 0.0.1dev)

eiogrplimit — Встановлює граничну кількість запитів у групі

### Опис

```methodsynopsis
eio_grp_limit(resource $grp, int $limit): void
```

Встановлює граничну кількість запитів групи.

### Список параметрів

`grp`

Покажчик на групу ресурсів

`limit`

Максимальна кількість ресурсів у групі.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [eiogrpadd()](function.eio-grp-add.md) - Додає запит до групи запитів
