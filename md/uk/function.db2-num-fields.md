---
navigation:
  - function.db2-next-result.md: « db2nextresult
  - function.db2-num-rows.md: db2numrows »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2numfields
---
# db2numfields

(PECL ibmdb2> = 1.0.0)

db2numfields — Повертає кількість полів у результуючому наборі

### Опис

```methodsynopsis
db2_num_fields(resource $stmt): int|false
```

Повертає кількість полів у результуючому наборі. Це корисно при обробці результуючих наборів динамічно сформованих запитів, або у разі використання процедур, що зберігаються.

### Список параметрів

`stmt`

Коректний ресурс оператора, що містить результуючий набір.

### Значення, що повертаються

Повертає кількість полів у результуючому наборі або **`false`**, якщо передано некоректний ресурс оператора.

### Приклади

**Приклад #1 Отримання кількості полів у результуючому наборі**

Наступний приклад демонструє отримання кількості полів у результуючому наборі.

```php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, $sql);
$columns = db2_num_fields($stmt);

echo "В результирующем наборе {$columns} столбцов.";
?>
```

Результат виконання цього прикладу:

```
В результирующем наборе 4 столбцов.
```

### Дивіться також

-   [db2execute()](function.db2-execute.md) - Виконує підготовлений SQL-запит
-   [db2fielddisplaysize()](function.db2-field-display-size.md) - Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2fieldname()](function.db2-field-name.md) - Повертає ім'я стовпця у наборі результатів
-   [db2fieldnum()](function.db2-field-num.md) - Повертає позицію зазначеного стовпця у наборі результатів
-   [db2fieldprecision()](function.db2-field-precision.md) - Повертає точність зазначеного стовпця у наборі результатів
-   [db2fieldscale()](function.db2-field-scale.md) - Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2fieldtype()](function.db2-field-type.md) - Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2fieldwidth()](function.db2-field-width.md) - Повертає ширину поточного значення вказаного стовпця у наборі результатів
