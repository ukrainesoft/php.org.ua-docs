Отримати кількість стовпців у результуючому наборі

-   [« cubrid\_list\_dbs](function.cubrid-list-dbs.html)
    
-   [cubrid\_ping »](function.cubrid-ping.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Отримати кількість стовпців у результуючому наборі
    

# cubridnumfields

(PECL CUBRID >= 8.3.0)

cubridnumfields — Отримати кількість стовпців у результуючому наборі

### Опис

```methodsynopsis
cubrid_num_fields(resource $result): int
```

Повертає кількість стовпців у результуючому наборі або **`false`** у разі виникнення помилки.

### Список параметрів

`result`

`result`, отриманий з [cubrid\_execute()](function.cubrid-execute.html) [cubrid\_query()](function.cubrid-query.html) або [cubrid\_prepare()](function.cubrid-prepare.html)

### Значення, що повертаються

Кількість стовпців у разі успішного виконання.

1, якщо SQL-запит був відмінним від SELECT типу.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridnumfields()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_fields($req);

printf("Количество строк: %d\nКоличество столбцов: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Количество строк: 6
Количество столбцов: 2
```