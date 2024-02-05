---
navigation:
  - function.variant-date-from-timestamp.md: « variant\_date\_from\_timestamp
  - function.variant-div.md: variant\_div »
  - index.md: PHP Manual
  - ref.com.md: Функції COM
title: variant\_date\_to\_timestamp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# variant\_date\_to\_timestamp

(PHP 5, PHP 7, PHP 8)

variant\_date\_to\_timestamp — Перетворює варіант типу дата/час у часову мітку Unix

### Опис

```methodsynopsis
variant_date_to_timestamp(variant $variant): ?int
```

Конвертує `variant`из значения\*\*`VT_DATE`\*\* (або аналогічного типу) у тимчасову мітку Unix. Це дозволяє простіше поєднати частину PHP у Unix-стилі з COM.

### Список параметрів

`variant`

Варіант.

### Значення, що повертаються

Повертає тимчасову мітку Unix або \*\*`null`\*\*в случае возникновения ошибки.

### Дивіться також

-   [variant\_date\_from\_timestamp()](function.variant-date-from-timestamp.md) \- Отримує подання дати для варіанта з мітки часу Unix
-   [date()](function.date.md) \- Форматує тимчасову мітку Unix
-   [strftime()](function.strftime.md) \- Форматує поточну дату/час з урахуванням поточних налаштувань локалі
