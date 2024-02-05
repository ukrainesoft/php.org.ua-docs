---
navigation:
  - function.variant-round.md: « variant\_round
  - function.variant-set.md: variant\_set »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_set\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_set\_type

(PHP 5, PHP 7, PHP 8)

variant\_set\_type — Наводить варіант до іншого типу «за місцем»

### Опис

```methodsynopsis
variant_set_type(variant $variant, int $type): void
```

Функція аналогічна функції [variant\_cast()](function.variant-cast.md) крім того, що змінюється сам варіант, а чи не створюється новий. Функції, що передаються, ідентичні параметрам функції [variant\_cast()](function.variant-cast.md)

### Список параметрів

`variant`

Варіант.

`type`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [variant\_cast()](function.variant-cast.md) \- Перетворює варіант на новий варіант іншого типу
-   [variant\_get\_type()](function.variant-get-type.md) \- Отримати тип варіанта
