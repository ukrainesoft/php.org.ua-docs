---
navigation:
  - function.cubrid-field-type.md: « cubrid\_field\_type
  - function.cubrid-num-fields.md: cubrid\_num\_fields »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_list\_dbs
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_list\_dbs

(PECL CUBRID >= 8.3.0)

cubrid\_list\_dbs — Отримати масив зі списком усіх баз даних CUBRID

### Опис

```methodsynopsis
cubrid_list_dbs(resource $conn_identifier = ?): array
```

Функція повертає масив зі списком усіх баз даних CUBRID

### Список параметрів

`conn_identifier`

The CUBRID connection.

### Значення, що повертаються

Індексований масив зі списком баз даних.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_list\_dbs()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$db_list = cubrid_list_dbs($conn);
var_dump($db_list);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  [0]=>
  string(6) "demodb"
}
```
