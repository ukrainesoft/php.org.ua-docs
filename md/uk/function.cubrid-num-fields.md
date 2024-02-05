---
navigation:
  - function.cubrid-list-dbs.md: « cubrid\_list\_dbs
  - function.cubrid-ping.md: cubrid\_ping »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_num\_fields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_num\_fields

(PECL CUBRID >= 8.3.0)

cubrid\_num\_fields — Отримати кількість стовпців у результуючому наборі

### Опис

```methodsynopsis
cubrid_num_fields(resource $result): int
```

Повертає кількість стовпців у результуючому наборі або \*\*`false`\*\*в случае возникновения ошибки.

### Список параметрів

`result`

`result`, отриманий з [cubrid\_execute()](function.cubrid-execute.md) [cubrid\_query()](function.cubrid-query.md) або [cubrid\_prepare()](function.cubrid-prepare.md)

### Значення, що повертаються

Кількість стовпців у разі успішного виконання.

\-1, якщо SQL-запит був відмінним від SELECT типу.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_num\_fields()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
Количество строк: 6
Количество столбцов: 2
```
