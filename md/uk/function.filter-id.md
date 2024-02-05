---
navigation:
  - function.filter-has-var.md: « filter\_has\_var
  - function.filter-input-array.md: filter\_input\_array »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filter\_id
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# filter\_id

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

filter\_id — Повертає ідентифікатор, який належить іменованому фільтру

### Опис

```methodsynopsis
filter_id(string $name): int|false
```

### Список параметрів

`name`

Ім'я фільтра.

### Значення, що повертаються

Ідентифікатор фільтра у разі успішного виконання або \*\*`false`\*\*якщо фільтр не існує.

### Дивіться також

-   [filter\_list()](function.filter-list.md) \- Повертає список усіх підтримуваних фільтрів
