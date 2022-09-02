---
navigation:
  - function.filter-has-var.md: « filterhasvar
  - function.filter-input-array.md: filterinputarray »
  - index.md: PHP Manual
  - ref.filter.md: Функції фільтрації даних
title: filterід
---
# filterід

(PHP 5> = 5.2.0, PHP 7, PHP 8)

filterid — Повертає ідентифікатор, який належить іменованому фільтру

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

-   [filterlist()](function.filter-list.md) - Повертає список усіх підтримуваних фільтрів
