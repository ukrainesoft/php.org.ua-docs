---
navigation:
  - function.ibase-num-fields.html: « ibasenumfields
  - function.ibase-param-info.html: ibaseparaminfo »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibasenumparams
---
# ibasenumparams

(PHP 5, PHP 7 < 7.4.0)

ibasenumparams — Повертає кількість параметрів у підготовленому запиті

### Опис

```methodsynopsis
ibase_num_params(resource $query): int
```

Ця функція повертає кількість параметрів у підготовленому запиті, вказаному `query`. Це кількість сполучних аргументів, які повинні бути присутніми під час виклику [ibaseexecute()](function.ibase-execute.md)

### Список параметрів

`query`

Дескриптор підготовленого запиту

### Значення, що повертаються

Повертає кількість параметрів як цілого числа.

### Дивіться також

-   [ibaseprepare()](function.ibase-prepare.md) - готує запит для подальшого зв'язування псевдозмінних та виконання
-   [ibaseparaminfo()](function.ibase-param-info.md) - Повертає інформацію про параметр у підготовленому запиті
