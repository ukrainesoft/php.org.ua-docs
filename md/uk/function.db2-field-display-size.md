---
navigation:
  - function.db2-fetch-row.md: « db2fetchrow
  - function.db2-field-name.md: db2fieldname »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2fielddisplaysize
---
# db2fielddisplaysize

(PECL ibmdb2> = 1.0.0)

db2fielddisplaysize — Повертає максимальну кількість байтів, необхідну для відображення стовпця

### Опис

```methodsynopsis
db2_field_display_size(resource $stmt, mixed $column): int
```

Повертає максимальну кількість байтів, необхідне відображення стовпця в наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає ціле значення з максимальною кількістю байтів, необхідних для відображення зазначеного стовпця. Якщо зазначений стовпець не існує у наборі результатів, **db2fielddisplaysize()** повертає **`false`**

### Дивіться також

-   [db2fieldname()](function.db2-field-name.md) - Повертає ім'я стовпця у наборі результатів
-   [db2fieldnum()](function.db2-field-num.md) - Повертає позицію зазначеного стовпця у наборі результатів
-   [db2fieldprecision()](function.db2-field-precision.md) - Повертає точність зазначеного стовпця у наборі результатів
-   [db2fieldscale()](function.db2-field-scale.md) - Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.md) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.md) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
