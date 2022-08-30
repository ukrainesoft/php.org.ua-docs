Отримує кількість елементів у стовпці типу колекція OID

-   [« cubridcolget](function.cubrid-col-get.html)
    
-   [cubridcolumnnames »](function.cubrid-column-names.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримує кількість елементів у стовпці типу колекція OID
    

# cubridcolsize

(PECL CUBRID >= 8.3.0)

cubridcolsize — Отримує кількість елементів у стовпці типу колекція OID

### Опис

```methodsynopsis
cubrid_col_size(resource $conn_identifier, string $oid, string $attr_name): int
```

Функція **cubridcolsize()** використовується для отримання кількості елементів в атрибуті типу колекції (set, multiset, sequence).

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра.

`attr_name`

Назва атрибута, з яким ви хочете працювати.

### Значення, що повертаються

Кількість елементів, у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                |
|--------|-----------------------------------------------------------------------------------------|
|        | Змінено значення, що повертається: у разі невдачі повертається **`false`**, а чи не -1. |

### Приклади

**Приклад #1 Приклад використання **cubridcolsize()****

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

$size = cubrid_col_size($conn, $oid, "b");
var_dump($size);

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
int(3)
```