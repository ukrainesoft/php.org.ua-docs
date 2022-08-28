Приведення варіанта до іншого типу "за місцем"

-   [« variant\_round](function.variant-round.html)
    
-   [variant\_set »](function.variant-set.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Приведення варіанта до іншого типу "за місцем"
    

# variantsettype

(PHP 5, PHP 7, PHP 8)

variantsettype — Приведення варіанта до іншого типу "за місцем"

### Опис

```methodsynopsis
variant_set_type(variant $variant, int $type): void
```

Функція аналогічна [variant\_cast()](function.variant-cast.html) крім того, що змінюється сам варіант, а чи не створюється новий. Функції, що передаються, ідентичні параметрам функції [variant\_cast()](function.variant-cast.html)

### Список параметрів

`variant`

Різновид.

`type`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [variant\_cast()](function.variant-cast.html) - Перетворення варіанта на новий варіант іншого типу
-   [variant\_get\_type()](function.variant-get-type.html) - Отримати тип варіанта