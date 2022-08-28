Вставляє один елемент для встановлення стовпця типу за допомогою OID

-   [« cubrid\_seq\_put](function.cubrid-seq-put.html)
    
-   [cubrid\_set\_autocommit »](function.cubrid-set-autocommit.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Вставляє один елемент для встановлення стовпця типу за допомогою OID
    

# cubridsetadd

(PECL CUBRID >= 8.3.0)

cubridsetadd — Вставляє один елемент для встановлення стовпця типу за допомогою OID

### Опис

```methodsynopsis
cubrid_set_add(    resource $conn_identifier,    string $oid,    string $attr_name,    string $set_element): bool
```

Функція **cubridsetadd()** використовується для вставки одного елемента заданий вами атрибут типу (set, multiset, sequence).

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, з яким ви хочете працювати.

`attr_name`

Ім'я атрибута, який потрібно вставити елемент.

`set_element`

Вміст елемента, який потрібно вставити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridsetadd()****

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

cubrid_set_add($conn, $oid, "b", "4");

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
array(4) {
  [0]=>
  string(1) "1"
  [1]=>
  string(1) "2"
  [2]=>
  string(1) "3"
  [3]=>
  string(1) "4"
}
```

### Дивіться також

-   [cubrid\_seq\_drop()](function.cubrid-seq-drop.html) - Видаляє елемент зі стовпця типу послідовності, використовуючи OID