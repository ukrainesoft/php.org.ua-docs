Отримати подання дати для варіанта з тимчасової мітки Unix

-   [« variantcmp](function.variant-cmp.html)
    
-   [variantdateтоtimestamp »](function.variant-date-to-timestamp.html)
    
-   [PHP Manual](index.html)
    
-   [Функции COM](ref.com.html)
    
-   Отримати подання дати для варіанта з тимчасової мітки Unix
    

# variantdatefromtimestamp

(PHP 5, PHP 7, PHP 8)

variantdatefromtimestamp — Отримати подання дати для варіанта з тимчасової мітки Unix

### Опис

```methodsynopsis
variant_date_from_timestamp(int $timestamp): variant
```

Перетворює `timestamp` зі значення тимчасової мітки Unix у варіант типу **`VT_DATE`**. Це дозволяє більш просто поєднати частину PHP у Unix-стилі з COM.

### Список параметрів

`timestamp`

Тимчасова мітка Unix.

### Значення, що повертаються

Повертає варіант типу **`VT_DATE`**

### Дивіться також

-   [variantdateтоtimestamp()](function.variant-date-to-timestamp.html) - Перетворює варіант типу дата/час у часову мітку Unix
-   [mktime()](function.mktime.html) - Повертає позначку часу Unix для заданої дати
-   [time()](function.time.html) - Повертає поточну мітку системного часу Unix