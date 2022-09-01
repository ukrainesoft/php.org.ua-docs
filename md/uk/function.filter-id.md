---
navigation:
  - function.filter-has-var.html: « filterhasvar
  - function.filter-input-array.html: filterinputarray »
  - index.html: PHP Manual
  - ref.filter.html: Функції фільтрації даних
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

-   [filterlist()](function.filter-list.html) - Повертає список усіх підтримуваних фільтрів
