---
navigation:
  - function.eio-grp-cancel.md: « eio\_grp\_cancel
  - function.eio-grp.md: eio\_grp »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_grp\_limit
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_grp\_limit

(PECL eio >= 0.0.1dev)

eio\_grp\_limit — Встановлює граничну кількість запитів у групі

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

-   [eio\_grp\_add()](function.eio-grp-add.md) \- Додає запит до групи запитів
