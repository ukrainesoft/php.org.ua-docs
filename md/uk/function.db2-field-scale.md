---
navigation:
  - function.db2-field-precision.html: « db2fieldprecision
  - function.db2-field-type.html: db2fieldtype »
  - index.md: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2fieldscale
---
# db2fieldscale

(PECL ibmdb2> = 1.0.0)

db2fieldscale — Повертає масштаб вказаного стовпця у наборі результатів

### Опис

```methodsynopsis
db2_field_scale(resource $stmt, mixed $column): int
```

Повертає масштаб вказаного стовпця у наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає ціле число, що містить масштаб вказаного стовпця. Якщо зазначений стовпець не існує у наборі результатів, **db2fieldscale()** повертає **`false`**

### Дивіться також

-   [db2fielddisplaysize()](function.db2-field-display-size.md) - Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2fieldname()](function.db2-field-name.md) - Повертає ім'я стовпця у наборі результатів
-   [db2fieldnum()](function.db2-field-num.md) - Повертає позицію зазначеного стовпця у наборі результатів
-   [db2fieldprecision()](function.db2-field-precision.md) - Повертає точність зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.md) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.md) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
