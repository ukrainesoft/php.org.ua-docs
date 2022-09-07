---
navigation:
  - function.variant-cmp.md: « variantcmp
  - function.variant-date-to-timestamp.md: variantdateтоtimestamp »
  - index.md: PHP Manual
  - ref.com.md: Функции COM
title: variantdatefromtimestamp
---
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

-   [variantdateтоtimestamp()](function.variant-date-to-timestamp.md) - Перетворює варіант типу дата/час у часову мітку Unix
-   [mktime()](function.mktime.md) - Повертає позначку часу Unix для заданої дати
-   [time()](function.time.md) - Повертає поточну мітку системного часу Unix
