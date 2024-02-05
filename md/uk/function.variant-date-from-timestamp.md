---
navigation:
  - function.variant-cmp.md: « variant\_cmp
  - function.variant-date-to-timestamp.md: variant\_date\_to\_timestamp »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_date\_from\_timestamp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_date\_from\_timestamp

(PHP 5, PHP 7, PHP 8)

variant\_date\_from\_timestamp — Отримує подання дати для варіанта з мітки часу Unix

### Опис

```methodsynopsis
variant_date_from_timestamp(int $timestamp): variant
```

Перетворює значення мітки часу Unix параметра `timestamp`в вариант типа\*\*`VT_DATE`\*\*. Це спрощує взаємодію між частинами PHP у Unix-стилі та COM.

### Список параметрів

`timestamp`

Тимчасова мітка Unix.

### Значення, що повертаються

Повертає варіант типу **`VT_DATE`**

### Дивіться також

-   [variant\_date\_to\_timestamp()](function.variant-date-to-timestamp.md) \- Перетворює варіант типу дата/час у часову мітку Unix
-   [mktime()](function.mktime.md) \- Повертає позначку часу Unix для заданої дати
-   [time()](function.time.md) \- Повертає поточну мітку системного часу Unix
