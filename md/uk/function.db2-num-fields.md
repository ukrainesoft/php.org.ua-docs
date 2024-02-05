---
navigation:
  - function.db2-next-result.md: « db2\_next\_result
  - function.db2-num-rows.md: db2\_num\_rows »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_num\_fields

(PECL ibm\_db2 >= 1.0.0)

db2\_num\_fields — Повертає кількість полів у результуючому наборі

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

Результат виконання наведеного прикладу:

```
В результирующем наборе 4 столбцов.
```

### Дивіться також

-   [db2\_execute()](function.db2-execute.md) \- Виконує підготовлений SQL-запит
-   [db2\_field\_display\_size()](function.db2-field-display-size.md) \- Повертає максимальну кількість байтів, необхідну для відображення стовпця
-   [db2\_field\_name()](function.db2-field-name.md) \- Повертає ім'я стовпця у наборі результатів
-   [db2\_field\_num()](function.db2-field-num.md) \- Повертає позицію зазначеного стовпця у наборі результатів
-   [db2\_field\_precision()](function.db2-field-precision.md) \- Повертає точність зазначеного стовпця у наборі результатів
-   [db2\_field\_scale()](function.db2-field-scale.md) \- Повертає масштаб зазначеного стовпця у наборі результатів
-   [db2\_field\_type()](function.db2-field-type.md) \- Повертає тип даних зазначеного стовпця у наборі результатів
-   [db2\_field\_width()](function.db2-field-width.md) \- Повертає ширину поточного значення вказаного стовпця у наборі результатів
