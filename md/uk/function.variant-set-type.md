---
navigation:
  - function.variant-round.html: « variantround
  - function.variant-set.html: variantset »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantsettype
---
# variantsettype

(PHP 5, PHP 7, PHP 8)

variantsettype — Приведення варіанта до іншого типу "за місцем"

### Опис

```methodsynopsis
variant_set_type(variant $variant, int $type): void
```

Функція аналогічна [variantcast()](function.variant-cast.html) крім того, що змінюється сам варіант, а чи не створюється новий. Функції, що передаються, ідентичні параметрам функції [variantcast()](function.variant-cast.html)

### Список параметрів

`variant`

Різновид.

`type`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [variantcast()](function.variant-cast.html) - Перетворення варіанта на новий варіант іншого типу
-   [variantgettype()](function.variant-get-type.html) - Отримати тип варіанта
