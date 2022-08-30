Отримати масив зі списком усіх баз даних CUBRID

-   [« cubridfieldtype](function.cubrid-field-type.html)
    
-   [cubridnumfields »](function.cubrid-num-fields.html)
    
-   [PHP Manual](index.md)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
    
-   Отримати масив зі списком усіх баз даних CUBRID
    

# cubridlistdbs

(PECL CUBRID >= 8.3.0)

cubridlistdbs — Отримати масив зі списком усіх баз даних CUBRID

### Опис

```methodsynopsis
cubrid_list_dbs(resource $conn_identifier = ?): array
```

Функція повертає масив зі списком усіх баз даних CUBRID

### Список параметрів

`conn_identifier`

CUBRID connection.

### Значення, що повертаються

Індексований масив зі списком баз даних.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridlistdbs()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$db_list = cubrid_list_dbs($conn);
var_dump($db_list);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(1) {
  [0]=>
  string(6) "demodb"
}
```