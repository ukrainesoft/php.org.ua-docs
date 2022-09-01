---
navigation:
  - function.db2-field-name.html: « db2fieldname
  - function.db2-field-precision.html: db2fieldprecision »
  - index.md: PHP Manual
  - ref.ibm-db2.html: Функції IBM DB2
title: db2fieldnum
---
# db2fieldnum

(PECL ibmdb2> = 1.0.0)

db2fieldnum — Повертає позицію зазначеного стовпця у наборі результатів

### Опис

```methodsynopsis
db2_field_num(resource $stmt, mixed $column): int
```

Повертає позицію зазначеного стовпця у наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає ціле число, що містить індекс (починаючи з 0) зазначеного стовпця набору результатів. Якщо зазначений стовпець не існує у наборі результатів, **db2fieldnum()** повертає **`false`**

### Дивіться також

-   [db2fielddisplaysize()](function.db2-field-display-size.md) - Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2fieldname()](function.db2-field-name.md) - Повертає ім'я стовпця у наборі результатів
-   [db2fieldprecision()](function.db2-field-precision.md) - Повертає точність зазначеного стовпця у наборі результатів
-   [db2fieldscale()](function.db2-field-scale.md) - Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.md) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.md) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
