Кількість рядків, порушених останнім SQL-запитом

-   [« Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   [cubrid\_client\_encoding »](function.cubrid-client-encoding.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Кількість рядків, порушених останнім SQL-запитом
    

# cubridaffectedrows

(PECL CUBRID >= 8.3.0)

cubridaffectedrows — Кількість рядків, порушених останнім SQL-запитом

### Опис

```methodsynopsis
cubrid_affected_rows(resource $conn_identifier = ?): int
```

```methodsynopsis
cubrid_affected_rows(resource $req_identifier = ?): int
```

Функція **cubridaffectedrows()** використовується для отримання кількості рядків, які торкнулися останнім SQL-запитом типу INSERT, DELETE або UPDATE.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання CUBRID. Якщо не задано, то використовуватиметься останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.html) з'єднання.

`req_identifier`

Ідентифікатор запиту має бути повернутий функціями [cubrid\_prepare()](function.cubrid-prepare.html) або [cubrid\_execute()](function.cubrid-execute.html). Якщо не заданий, буде використано останній запит, повернутий [cubrid\_prepare()](function.cubrid-prepare.html) або [cubrid\_execute()](function.cubrid-execute.html)

### Значення, що повертаються

Кількість рядків, які торкнулися останнім SQL-запитом, у разі успішного виконання.

1, якщо запит не був типом INSERT, DELETE або UPDATE.

**`false`**, якщо ідентифікатор запиту не вказано та відсутні будь-які виконані запити.

### Приклади

**Приклад #1 Приклад використання **cubridaffectedrows()****

```php
<?php
$conn = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
cubrid_execute($conn, "DROP TABLE IF EXISTS cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (d varchar)");
$sql_stmt = "INSERT INTO cubrid_test(d) VALUES('php-test')";
$req = cubrid_prepare($conn, $sql_stmt);

for ($i = 0; $i < 10; $i++) {
    cubrid_execute($req);
}
cubrid_commit($conn);

$req = cubrid_execute($conn, "DELETE FROM cubrid_test WHERE d='php-test'", CUBRID_ASYNC);
var_dump(cubrid_affected_rows());
var_dump(cubrid_affected_rows($conn));
var_dump(cubrid_affected_rows($req));

cubrid_disconnect($conn);

print "done!";
?>
```

Результат виконання цього прикладу:

```
Rows deleted: 5
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор