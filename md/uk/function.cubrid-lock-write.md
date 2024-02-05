---
navigation:
  - function.cubrid-lock-read.md: « cubrid\_lock\_read
  - function.cubrid-move-cursor.md: cubrid\_move\_cursor »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lock\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lock\_write

(PECL CUBRID >= 8.3.0)

cubrid\_lock\_write — Встановлює блокування запису для цього OID

### Опис

```methodsynopsis
cubrid_lock_write(resource $conn_identifier, string $oid): bool
```

Функция**cubrid\_lock\_write()** використовується для встановлення блокування запису екземпляра, на який вказує даний `oid`

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, на який необхідно встановити блокування запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_lock\_write()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

cubrid_lock_write($conn, $oid);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_put($conn, $oid, "b", array(2, 4, 8));

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  string(1) "1"
  [1]=>
  string(1) "2"
  [2]=>
  string(1) "3"
}
array(3) {
  [0]=>
  string(1) "2"
  [1]=>
  string(1) "4"
  [2]=>
  string(1) "8"
}
```

### Дивіться також

-   [cubrid\_lock\_read()](function.cubrid-lock-read.md) \- Встановлює блокування читання для цього OID
