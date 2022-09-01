---
navigation:
  - function.db2-field-display-size.html: « db2fielddisplaysize
  - function.db2-field-num.html: db2fieldnum »
  - index.md: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2fieldname
---
# db2fieldname

(PECL ibmdb2> = 1.0.0)

db2fieldname — Повертає ім'я стовпця у наборі результатів

### Опис

```methodsynopsis
db2_field_name(resource $stmt, mixed $column): string
```

Повертає ім'я зазначеного стовпця у наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає рядок, який містить ім'я зазначеного стовпця. Якщо зазначений стовпець не існує у наборі результатів, **db2fieldname()** повертає **`false`**

### Дивіться також

-   [db2fielddisplaysize()](function.db2-field-display-size.html) - Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2fieldnum()](function.db2-field-num.html) - Повертає позицію зазначеного стовпця у наборі результатів
-   [db2fieldprecision()](function.db2-field-precision.html) - Повертає точність зазначеного стовпця у наборі результатів
-   [db2fieldscale()](function.db2-field-scale.html) - Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.html) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.html) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
