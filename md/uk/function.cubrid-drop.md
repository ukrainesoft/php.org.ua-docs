---
navigation:
  - function.cubrid-disconnect.md: « cubrid\_disconnect
  - function.cubrid-error-code-facility.md: cubrid\_error\_code\_facility »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_drop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_drop

(PECL CUBRID >= 8.3.0)

cubrid\_drop — Видалення екземпляра OID

### Опис

```methodsynopsis
cubrid_drop(resource $conn_identifier, string $oid): bool
```

Функция**cubrid\_drop()** використовується для видалення екземпляра з бази даних, заданого його `oid`

### Список параметрів

`conn_identifier`

Connection identifier.

`oid`

Oid екземпляра, який треба видалити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_drop()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

printf("--- Before Drop: ---\n");
$attr = cubrid_get($conn, $oid);
var_dump($attr);

if (cubrid_drop($conn, $oid)) {
    cubrid_commit($conn);
} else {
    cubrid_rollback($conn);
}

cubrid_close_request($req);

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

printf("\n--- After Drop: ---\n");
$attr = cubrid_get($conn, $oid);
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
--- Before Drop: ---
array(4) {
  ["a"]=>
  string(1) "1"
  ["b"]=>
  array(3) {
    [0]=>
    string(1) "1"
    [1]=>
    string(1) "2"
    [2]=>
    string(1) "3"
  }
  ["c"]=>
  array(4) {
    [0]=>
    string(2) "11"
    [1]=>
    string(2) "22"
    [2]=>
    string(2) "33"
    [3]=>
    string(3) "333"
  }
  ["d"]=>
  string(10) "a         "
}

--- After Drop: ---
array(4) {
  ["a"]=>
  string(1) "2"
  ["b"]=>
  array(3) {
    [0]=>
    string(1) "4"
    [1]=>
    string(1) "5"
    [2]=>
    string(1) "7"
  }
  ["c"]=>
  array(4) {
    [0]=>
    string(2) "44"
    [1]=>
    string(2) "55"
    [2]=>
    string(2) "66"
    [3]=>
    string(3) "666"
  }
  ["d"]=>
  string(10) "b         "
}
```

### Дивіться також

-   [cubrid\_is\_instance()](function.cubrid-is-instance.md) \- Перевіряє, чи існує екземпляр, на який вказує OID
