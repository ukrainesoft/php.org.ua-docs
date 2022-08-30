Повертає один стовпець з рядка у наборі результатів

-   [« db2procedures](function.db2-procedures.html)
    
-   [db2rollback »](function.db2-rollback.html)
    
-   [PHP Manual](index.md)
    
-   [Функції IBM DB2](ref.ibm-db2.html)
    
-   Повертає один стовпець з рядка у наборі результатів
    

# db2result

(PECL ibmdb2> = 1.0.0)

db2result — Повертає один стовпець із рядка у наборі результатів

### Опис

```methodsynopsis
db2_result(resource $stmt, mixed $column): mixed
```

Використовуйте **db2result()**, щоб повернути значення вказаного стовпця у поточному рядку набору результатів. Ви повинні викликати [db2fetchrow()](function.db2-fetch-row.html) перед викликом **db2result()**, щоб встановити положення покажчика набору результатів.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`

`column`

Або цілий індекс стовпця (починаючи з 0) у наборі результатів, або рядок, що відповідає імені стовпця.

### Значення, що повертаються

Повертає значення запитаного поля, якщо поле існує у наборі результатів. Повертає NULL, якщо поле не існує та видає попередження.

### Приклади

**Приклад #1 Приклад використання **db2result()****

У наступному прикладі показано, як виконати ітерацію по набору результатів за допомогою [db2fetchrow()](function.db2-fetch-row.html) та отримати стовпці з набору результатів за допомогою **db2result()**

```php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 'BREED');
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

### Дивіться також

-   [db2fetcharray()](function.db2-fetch-array.html) - Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2fetchassoc()](function.db2-fetch-assoc.html) - Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів
-   [db2fetchboth()](function.db2-fetch-both.html) - Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2fetchobject()](function.db2-fetch-object.html) - Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2fetchrow()](function.db2-fetch-row.html) - Встановлює вказівник набору результатів на наступний рядок або запрошений рядок