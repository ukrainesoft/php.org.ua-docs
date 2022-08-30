Перетворення варіанта на новий варіант іншого типу

-   [« variantand](function.variant-and.html)
    
-   [variantcat »](function.variant-cat.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Перетворення варіанта на новий варіант іншого типу
    

# variantcast

(PHP 5, PHP 7, PHP 8)

variantcast — Перетворення варіанта на новий варіант іншого типу

### Опис

```methodsynopsis
variant_cast(variant $variant, int $type): variant
```

Функція робить копію варіанта `variant` і перетворює її до типу `type`

Функція є обгорткою над функцією VariantChangeType() із бібліотеки COM. Докладніше читайте у MSDN.

### Список параметрів

`variant`

Різновид.

`type`

`type` має бути однією з констант **`VT_XXX`**

### Значення, що повертаються

Повертає варіант заданого типу `type`

### Дивіться також

-   [variantsettype()](function.variant-set-type.html) - Приведення варіанта до іншого типу "за місцем"