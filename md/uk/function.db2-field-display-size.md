---
navigation:
  - function.db2-fetch-row.md: « db2\_fetch\_row
  - function.db2-field-name.md: db2\_field\_name »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_field\_display\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_field\_display\_size

(PECL ibm\_db2 >= 1.0.0)

db2\_field\_display\_size — Повертає максимальну кількість байтів, необхідну для відображення стовпця

### Опис

```methodsynopsis
db2_field_display_size(resource $stmt, int|string $column): int|false
```

Повертає максимальну кількість байтів, необхідне відображення стовпця в наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає ціле значення з максимальною кількістю байтів, необхідних для відображення зазначеного стовпця. Якщо зазначений стовпець не існує у наборі результатів, **db2\_field\_display\_size()** повертає **`false`**

### Дивіться також

-   [db2\_field\_name()](function.db2-field-name.md) \- Повертає ім'я стовпця у наборі результатів
-   [db2\_field\_num()](function.db2-field-num.md) \- Повертає позицію зазначеного стовпця у наборі результатів
-   [db2\_field\_precision()](function.db2-field-precision.md) \- Повертає точність зазначеного стовпця у наборі результатів
-   [db2\_field\_scale()](function.db2-field-scale.md) \- Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2\_field\_type()](function.db2-field-type.md) \- Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2\_field\_width()](function.db2-field-width.md) \- Повертає ширину поточного значення вказаного стовпця у наборі результатів
