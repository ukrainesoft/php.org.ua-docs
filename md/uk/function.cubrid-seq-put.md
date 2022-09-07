---
navigation:
  - function.cubrid-seq-insert.md: « cubridseqinsert
  - function.cubrid-set-add.md: cubridsetadd »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridseqput
---
# cubridseqput

(PECL CUBRID >= 8.3.0)

cubridseqput — Оновлення значення елемента стовпця типу послідовності за допомогою OID

### Опис

```methodsynopsis
cubrid_seq_put(    resource $conn_identifier,    string $oid,    string $attr_name,    int $index,    string $seq_element): bool
```

Функція **cubridseqput()** використовується для оновлення вмісту запитаного елемента в атрибуті sequent type за допомогою OID.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, з яким ви хочете працювати.

`attr_name`

Ім'я атрибута ви хочете оновити елемент.

`index`

Індекс (починаючи з 1) елемент, який ви хочете оновити.

`seq_element`

Новий контент, який потрібно використовувати для оновлення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridseqput()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c sequence(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_seq_put($conn, $oid, "c", 1, "111");

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
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
array(4) {
  [0]=>
  string(3) "111"
  [1]=>
  string(2) "22"
  [2]=>
  string(2) "33"
  [3]=>
  string(3) "333"
}
```

### Дивіться також

-   [cubridseqdrop()](function.cubrid-seq-drop.md) - Видаляє елемент зі стовпця типу послідовності, використовуючи OID
-   [cubridseqinsert()](function.cubrid-seq-insert.md) - Вставляє елемент у стовпець типу послідовності, використовуючи OID
