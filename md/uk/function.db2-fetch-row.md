Встановлює вказівник набору результатів на наступний рядок або запрошений рядок

-   [« db2\_fetch\_object](function.db2-fetch-object.html)
    
-   [db2\_field\_display\_size »](function.db2-field-display-size.html)
    
-   [PHP Manual](index.html)
    
-   [Функции IBM DB2](ref.ibm-db2.html)
    
-   Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
    

# db2fetchrow

(PECL ibmdb2> = 1.0.0)

db2fetchrow — Встановлює вказівник набору результатів на наступний рядок або запрошений рядок

### Опис

```methodsynopsis
db2_fetch_row(resource $stmt, int $row_number = ?): bool
```

Використовуйте **db2fetchrow()** для ітерації за набором результатів або для вказівки на певний рядок у наборі результатів, якщо ви запросили курсор, що прокручується.

Щоб отримати окремі поля із набору результатів, викличте функцію [db2\_result()](function.db2-result.html)

Замість викликати **db2fetchrow()** і [db2\_result()](function.db2-result.html), більшість програм буде викликати одну з функцій [db2\_fetch\_assoc()](function.db2-fetch-assoc.html) [db2\_fetch\_both()](function.db2-fetch-both.html) або [db2\_fetch\_array()](function.db2-fetch-array.html), щоб просунути покажчик набору результатів та повернути повний рядок у вигляді масиву.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`

`row_number`

За допомогою курсорів, що прокручуються, ви можете запросити конкретний номер рядка в наборі результатів. Нумерація рядків починається з першого.

### Значення, що повертаються

Повертає **`true`**, якщо запитаний рядок існує у наборі результатів. Повертає **`false`**, якщо запрошений рядок не існує у наборі результатів.

### Приклади

**Приклад #1 Ітерації з набору результатів**

У наступному прикладі показано, як виконати ітерацію по набору результатів за допомогою **db2fetchrow()** та отримати стовпці з набору результатів за допомогою [db2\_result()](function.db2-result.html)

```php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 1);
    print "$name $breed";
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

В i5/OS рекомендується використовувати [db2\_fetch\_both()](function.db2-fetch-both.html) [db2\_fetch\_array()](function.db2-fetch-array.html) або [db2\_fetch\_object()](function.db2-fetch-object.html) замість **db2fetchrow()**[db2\_result()](function.db2-result.html). Зазвичай у **db2fetchrow()**[db2\_result()](function.db2-result.html) більше проблем з різними типами стовпців під час перетворення `EBCIDIC` в `ASCII`, включаючи можливе усічення в `DBCS` додатках. Ви також можете виявити, що продуктивність [db2\_fetch\_both()](function.db2-fetch-both.html) [db2\_fetch\_array()](function.db2-fetch-array.html) і [db2\_fetch\_object()](function.db2-fetch-object.html) перевершує **db2fetchrow()**[db2\_result()](function.db2-result.html)

```php
<?php
  $conn = db2_connect("","","");
  $sql = 'SELECT SPECIFIC_SCHEMA, SPECIFIC_NAME, ROUTINE_SCHEMA, ROUTINE_NAME, ROUTINE_TYPE, ROUTINE_CREATED, ROUTINE_BODY, IN_PARMS, OUT_PARMS, INOUT_PARMS, PARAMETER_STYLE, EXTERNAL_NAME, EXTERNAL_LANGUAGE FROM QSYS2.SYSROUTINES FETCH FIRST 2 ROWS ONLY';
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_both($stmt)){
    echo "<br>db2_fetch_both {$row['SPECIFIC_NAME']} {$row['ROUTINE_CREATED']} {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_array($stmt)){
    echo "<br>db2_fetch_array {$row[1]}  {$row[5]}";
  }
  $stmt = db2_exec($conn, $sql, array('cursor' => DB2_SCROLLABLE));
  while ($row = db2_fetch_object($stmt)){
    echo "<br>db2_fetch_object {$row->SPECIFIC_NAME} {$row->ROUTINE_CREATED}";
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

-   [db2\_fetch\_array()](function.db2-fetch-array.html) - Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_assoc()](function.db2-fetch-assoc.html) - Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_both()](function.db2-fetch-both.html) - Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2\_fetch\_object()](function.db2-fetch-object.html) - Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2\_result()](function.db2-result.html) - Повертає один стовпець з рядка у наборі результатів