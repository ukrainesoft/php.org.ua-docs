Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні

-   [« db2getoption](function.db2-get-option.html)
    
-   [db2lobread »](function.db2-lob-read.html)
    
-   [PHP Manual](index.html)
    
-   [Функції IBM DB2](ref.ibm-db2.html)
    
-   Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні
    

# db2lastinsertід

(PECL ibmdb2> = 1.7.1)

db2lastinsertid — Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні

### Опис

```methodsynopsis
db2_last_insert_id(resource $resource): string
```

Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні.

На результат цієї функції не впливає жодна з наступних:

-   Оператор INSERT для одного рядка з VALUES для таблиці без стовпчика ідентифікаторів.
    
-   Оператор INSERT для кількох рядків із VALUES.
    
-   Оператор INSERT із повною вибіркою.
    
-   Оператор ROLLBACK TO SAVEPOINT
    

### Список параметрів

`resource`

Допустимий ресурс підключення, що повертається [db2connect()](function.db2-connect.html) або [db2pconnect()](function.db2-pconnect.html). Значення цього параметра може бути ресурсом оператора чи ресурсом набору результатів.

### Значення, що повертаються

Повертає автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні.

### Приклади

**Приклад #1 Приклад використання **db2lastinsertid()****

У наступному прикладі показано, як повернути автоматично згенерований ідентифікатор останнього запиту додавання, успішно виконаного в цьому з'єднанні.

```php
<?php

$database = "SAMPLE";
$user = "db2inst1";
$password = "ibmdb2";

$conn = db2_connect($database, $user, $password);
if($conn) {
    $createTable = "CREATE TABLE lastInsertID
      (id integer GENERATED BY DEFAULT AS IDENTITY, name varchar(20))";
    $insertTable = "INSERT INTO lastInsertID (name) VALUES ('Temp Name')";

    $stmt = @db2_exec($conn, $createTable);

    /* Проверка на вставку одной строки. */
    $stmt = db2_exec($conn, $insertTable);
    $ret =  db2_last_insert_id($conn);
    if($ret) {
        echo "Последний идентификатор : " . $ret . "\n";
    } else {
        echo "Последний идентификатор отсутствует.\n";
    }

    db2_close($conn);
}
else {
    echo "Ошибка соединения.";
}
?>
```

Результат виконання цього прикладу:

```
Последний идентификатор : 1
```