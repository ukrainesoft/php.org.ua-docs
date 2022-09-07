---
navigation:
  - function.db2-fetch-object.md: « db2fetchobject
  - function.db2-field-display-size.md: db2fielddisplaysize »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2fetchrow
---
# db2fetchrow

(PECL ibmdb2> = 1.0.0)

db2fetchrow — Встановлює вказівник набору результатів на наступний рядок або запрошений рядок

### Опис

```methodsynopsis
db2_fetch_row(resource $stmt, int $row_number = ?): bool
```

Використовуйте **db2fetchrow()** для ітерації за набором результатів або для вказівки на певний рядок у наборі результатів, якщо ви запросили курсор, що прокручується.

Щоб отримати окремі поля із набору результатів, викличте функцію [db2result()](function.db2-result.md)

Замість викликати **db2fetchrow()** і [db2result()](function.db2-result.md), більшість програм буде викликати одну з функцій [db2fetchassoc()](function.db2-fetch-assoc.md) [db2fetchboth()](function.db2-fetch-both.md) або [db2fetcharray()](function.db2-fetch-array.md), щоб просунути покажчик набору результатів та повернути повний рядок у вигляді масиву.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`

`row_number`

За допомогою курсорів, що прокручуються, ви можете запросити конкретний номер рядка в наборі результатів. Нумерація рядків починається з першого.

### Значення, що повертаються

Повертає **`true`**, якщо запитаний рядок існує у наборі результатів. Повертає **`false`**, якщо запрошений рядок не існує у наборі результатів.

### Приклади

**Приклад #1 Ітерації з набору результатів**

У наступному прикладі показано, як виконати ітерацію по набору результатів за допомогою **db2fetchrow()** та отримати стовпці з набору результатів за допомогою [db2result()](function.db2-result.md)

```php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 1);
    print "$name $breed";
}
?>
```

Результат виконання цього прикладу:

```
cat Pook
gold fish Bubbles
budgerigar Gizmo
goat Rickety Ride
```

**Приклад #2 Рекомендовані альтернативи db2fetchrow/db2result для i5/OS**

В i5/OS рекомендується використовувати [db2fetchboth()](function.db2-fetch-both.md) [db2fetcharray()](function.db2-fetch-array.md) або [db2fetchobject()](function.db2-fetch-object.md) замість **db2fetchrow()**[db2result()](function.db2-result.md). Зазвичай у **db2fetchrow()**[db2result()](function.db2-result.md) більше проблем з різними типами стовпців під час перетворення `EBCIDIC` в `ASCII`, включаючи можливе усічення в `DBCS` додатках. Ви також можете виявити, що продуктивність [db2fetchboth()](function.db2-fetch-both.md) [db2fetcharray()](function.db2-fetch-array.md) і [db2fetchobject()](function.db2-fetch-object.md) перевершує **db2fetchrow()**[db2result()](function.db2-result.md)

```php
<?php
  $conn = db2_connect("","","");
  $sql = 'SELECT SPECIFIC_SCHEMA, SPECIFIC_NAME, ROUTINE_SCHEMA, ROUTINE_NAME, ROUTINE_TYPE, ROUTINE_CREATED, ROUTINE_BODY, IN_PARMS, OUT_PARMS, INOUT_PARMS, PARAMETER_STYLE, EXTERNAL_NAME, EXTERNAL_LANGUAGE FROM QSYS2.SYSROUTINES FETCH FIRST 2 ROWS ONLY';
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_both($stmt)){
    echo "<br>db2_fetch_both {$row['SPECIFIC_NAME']} {$row['ROUTINE_CREATED']} {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_array($stmt)){
    echo "<br>db2_fetch_array {$row[1]}  {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_object($stmt)){
    echo "<br>db2_fetch_object {$row->SPECIFIC_NAME} {$row->ROUTINE_CREATED}";
  }
  db2_close($conn);
?>
```

Результат виконання цього прикладу:

```
db2_fetch_both MATCH_ANIMAL 2006-08-25-17.10.23.775000 2006-08-25-17.10.23.775000
db2_fetch_both MULTIRESULTS 2006-10-17-10.11.05.308000 2006-10-17-10.11.05.308000
db2_fetch_array MATCH_ANIMAL 2006-08-25-17.10.23.775000
db2_fetch_array MULTIRESULTS 2006-10-17-10.11.05.308000
db2_fetch_object MATCH_ANIMAL 2006-08-25-17.10.23.775000
db2_fetch_object MULTIRESULTS 2006-10-17-10.11.05.308000
```

### Дивіться також

-   [db2fetcharray()](function.db2-fetch-array.md) - Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2fetchassoc()](function.db2-fetch-assoc.md) - Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів
-   [db2fetchboth()](function.db2-fetch-both.md) - Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2fetchobject()](function.db2-fetch-object.md) - Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2result()](function.db2-result.md) - Повертає один стовпець з рядка у наборі результатів
