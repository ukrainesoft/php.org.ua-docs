---
navigation:
  - function.ibase-num-fields.md: « ibase\_num\_fields
  - function.ibase-param-info.md: ibase\_param\_info »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_num\_params
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_num\_params

(PHP 5, PHP 7 < 7.4.0)

ibase\_num\_params — Повертає кількість параметрів у підготовленому запиті

### Опис

```methodsynopsis
ibase_num_params(resource $query): int
```

Ця функція повертає кількість параметрів у підготовленому запиті, вказаному `query`. Це кількість сполучних аргументів, які повинні бути присутніми під час виклику [ibase\_execute()](function.ibase-execute.md)

### Список параметрів

`query`

Дескриптор підготовленого запиту

### Значення, що повертаються

Повертає кількість параметрів як цілого числа.

### Дивіться також

-   [ibase\_prepare()](function.ibase-prepare.md) \- готує запит для подальшого зв'язування псевдозмінних та виконання
-   [ibase\_param\_info()](function.ibase-param-info.md) \- Повертає інформацію про параметр у підготовленому запиті
