---
navigation:
  - function.cubrid-list-dbs.md: « cubridlistdbs
  - function.cubrid-ping.md: cubridping »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridnumfields
---
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

`result`, отриманий з [cubridexecute()](function.cubrid-execute.md) [cubridquery()](function.cubrid-query.md) або [cubridprepare()](function.cubrid-prepare.md)

### Значення, що повертаються

Кількість стовпців у разі успішного виконання.

1, якщо SQL-запит був відмінним від SELECT типу.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridnumfields()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_fields($req);

printf("Количество строк: %d\nКоличество столбцов: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Количество строк: 6
Количество столбцов: 2
```
