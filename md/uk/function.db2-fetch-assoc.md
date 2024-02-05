---
navigation:
  - function.db2-fetch-array.md: « db2\_fetch\_array
  - function.db2-fetch-both.md: db2\_fetch\_both »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_fetch\_assoc

(PECL ibm\_db2 >= 1.0.0)

db2\_fetch\_assoc — Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів

### Опис

```methodsynopsis
db2_fetch_assoc(resource $stmt, int $row_number = -1): array|false
```

Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`містить набір результатів.

`row_number`

Запитує конкретний рядок за індексом (починається з 1) із набору результатів. Передача параметра призводить до запобігання PHP, якщо в наборі результатів використовується курсор "forward-only".

### Значення, що повертаються

Повертає асоціативний масив зі значеннями стовпців, проіндексованими на ім'я стовпця, що представляє наступний або запитаний рядок у наборі результатів. Повертає **`false`**, якщо в наборі результатів не залишилося рядків або якщо рядок, запитаний `row_number`, немає в наборі результатів.

### Приклади

**Приклад #1 Перебір курсором forward-only**

Якщо ви викликаєте **db2\_fetch\_assoc()** без певного номера рядка, він автоматично отримує наступний рядок у наборі результатів.

```php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$stmt = db2_prepare($conn, $sql);
$result = db2_execute($stmt);

while ($row = db2_fetch_assoc($stmt)) {
    printf ("%-5d %-16s %-32s %10s\n",
        $row['ID'], $row['NAME'], $row['BREED'], $row['WEIGHT']);
}
?>
```

Результат виконання наведеного прикладу:

```
0     Pook             cat                                    3.20
5     Rickety Ride     goat                                   9.70
2     Smarty           horse                                350.00
```

\*\*Приклад #2 Отримання певних рядків за допомогою \*\*db2\_fetch\_assoc()**из прокручиваемого курсора**

Якщо у вашому наборі результатів використовується курсор, що прокручується, ви можете викликати **db2\_fetch\_assoc()** з певним номером рядка. У наступному прикладі витягується кожен другий рядок у наборі результатів, починаючи з другого рядка.

```php
<?php

$sql = "SELECT id, name, breed, weight FROM animals ORDER BY breed";
$result = db2_exec($stmt, $sql, array('cursor' => DB2_SCROLLABLE));

$i=2;
while ($row = db2_fetch_assoc($result, $i)) {
    printf ("%-5d %-16s %-32s %10s\n",
        $row['ID'], $row['NAME'], $row['BREED'], $row['WEIGHT']);
    $i = $i + 2;
}
?>
```

Результат виконання наведеного прикладу:

```
0     Pook             cat                                    3.20
5     Rickety Ride     goat                                   9.70
2     Smarty           horse                                350.00
```

### Дивіться також

-   [db2\_fetch\_array()](function.db2-fetch-array.md) \- Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_both()](function.db2-fetch-both.md) \- Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2\_fetch\_object()](function.db2-fetch-object.md) \- Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2\_fetch\_row()](function.db2-fetch-row.md) \- Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
-   [db2\_result()](function.db2-result.md) \- Повертає один стовпець з рядка у наборі результатів
