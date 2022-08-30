Перетворює варіант типу дата/час у часову мітку Unix

-   [« variantdatefromtimestamp](function.variant-date-from-timestamp.html)
    
-   [variantdiv »](function.variant-div.html)
    
-   [PHP Manual](index.md)
    
-   [Функции COM](ref.com.md)
    
-   Перетворює варіант типу дата/час у часову мітку Unix
    

# variantdateтоtimestamp

(PHP 5, PHP 7, PHP 8)

variantdateтоtimestamp — Перетворює варіант типу дата/час у часову мітку Unix

### Опис

```methodsynopsis
variant_date_to_timestamp(variant $variant): ?int
```

Конвертує `variant` зі значення **`VT_DATE`** (або аналогічного типу) у тимчасову мітку Unix. Це дозволяє простіше поєднати частину PHP у Unix-стилі з COM.

### Список параметрів

`variant`

Різновид.

### Значення, що повертаються

Повертає тимчасову мітку Unix або **`null`** у разі виникнення помилки.

### Дивіться також

-   [variantdatefromtimestamp()](function.variant-date-from-timestamp.html) - Отримати подання дати для варіанта з тимчасової мітки Unix
-   [date()](function.date.md) - Форматує тимчасову мітку Unix
-   [strftime()](function.strftime.md) - Форматує поточну дату/час з урахуванням поточних налаштувань локалі