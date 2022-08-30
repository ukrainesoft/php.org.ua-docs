Приведення варіанта до іншого типу "за місцем"

-   [« variantround](function.variant-round.html)
    
-   [variantset »](function.variant-set.html)
    
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