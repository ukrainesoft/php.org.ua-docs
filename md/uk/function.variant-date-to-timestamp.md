Перетворює варіант типу дата/час у часову мітку Unix

-   [« variant\_date\_from\_timestamp](function.variant-date-from-timestamp.html)
    
-   [variant\_div »](function.variant-div.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
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

-   [variant\_date\_from\_timestamp()](function.variant-date-from-timestamp.html) - Отримати подання дати для варіанта з тимчасової мітки Unix
-   [date()](function.date.html) - Форматує тимчасову мітку Unix
-   [strftime()](function.strftime.html) - Форматує поточну дату/час з урахуванням поточних налаштувань локалі