Видаляє елемент із стовпця заданого типу, використовуючи OID

-   [« cubridsetдбparameter](function.cubrid-set-db-parameter.html)
    
-   [cubridsetquerytimeout »](function.cubrid-set-query-timeout.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Видаляє елемент із стовпця заданого типу, використовуючи OID
    

# cubridsetdrop

(PECL CUBRID >= 8.3.0)

cubridsetdrop — Видаляє елемент із стовпця заданого типу, використовуючи OID

### Опис

```methodsynopsis
cubrid_set_drop(    resource $conn_identifier,    string $oid,    string $attr_name,    string $set_element): bool
```

Функція **cubridsetdrop()** використовується для видалення елемента, який ви запитуєте із заданого атрибута типу набору (set, multiset) бази даних.

### Список параметрів

`conn_identifier`

Connection identifier.

`oid`

OID екземпляра, з яким ви хочете працювати.

`attr_name`

Ім'я атрибута, з якого ви бажаєте видалити елемент.

`set_element`

Вміст елемента, який потрібно видалити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridsetdrop()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_set_drop($conn, $oid, "b", "1");

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(3) {
  [0]=>
  string(1) "1"
  [1]=>
  string(1) "2"
  [2]=>
  string(1) "3"
}
array(2) {
  [0]=>
  string(1) "2"
  [1]=>
  string(1) "3"
}
```

### Дивіться також

-   [cubridsetadd()](function.cubrid-set-add.html) - Вставляє один елемент для встановлення стовпця типу за допомогою OID