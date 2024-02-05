---
navigation:
  - function.variant-and.md: « variant\_and
  - function.variant-cat.md: variant\_cat »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_cast
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_cast

(PHP 5, PHP 7, PHP 8)

variant\_cast — Перетворює варіант на новий варіант іншого типу

### Опис

```methodsynopsis
variant_cast(variant $variant, int $type): variant
```

Функція робить копію варіанта `variant` і перетворює її до типу `type`

Ця функція – обгортка над функцією VariantChangeType() з бібліотеки COM; докладніше про це розповідається у документації MSDN.

### Список параметрів

`variant`

Варіант.

`type`

`type` має бути однією з констант **`VT_XXX`**

### Значення, що повертаються

Повертає варіант заданого у параметрі `type`типа.

### Дивіться також

-   [variant\_set\_type()](function.variant-set-type.md) \- Наводить варіант до іншого типу «за місцем»
