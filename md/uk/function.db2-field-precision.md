---
navigation:
  - function.db2-field-num.md: « db2fieldnum
  - function.db2-field-scale.md: db2fieldscale »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2fieldprecision
---
# db2fieldprecision

(PECL ibmdb2> = 1.0.0)

db2fieldprecision — Повертає точність зазначеного стовпця у наборі результатів

### Опис

```methodsynopsis
db2_field_precision(resource $stmt, mixed $column): int
```

Повертає точність зазначеного стовпця у наборі результатів.

### Список параметрів

`stmt`

Задає ресурс оператора, що містить набір результатів.

`column`

Задає стовпець у наборі результатів. Це може бути ціле число, що представляє індекс шпальти (починаючи з 0) або рядок, що містить ім'я шпальти.

### Значення, що повертаються

Повертає ціле число, що містить точність зазначеного стовпця. Якщо зазначений стовпець не існує у наборі результатів, **db2fieldprecision()** повертає **`false`**

### Дивіться також

-   [db2fielddisplaysize()](function.db2-field-display-size.md) - Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2fieldname()](function.db2-field-name.md) - Повертає ім'я стовпця у наборі результатів
-   [db2fieldnum()](function.db2-field-num.md) - Повертає позицію зазначеного стовпця у наборі результатів
-   [db2fieldscale()](function.db2-field-scale.md) - Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.md) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.md) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
