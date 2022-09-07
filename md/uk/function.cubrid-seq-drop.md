---
navigation:
  - function.cubrid-schema.md: « cubridschema
  - function.cubrid-seq-insert.md: cubridseqinsert »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridseqdrop
---
# cubridseqdrop

(PECL CUBRID >= 8.3.0)

cubridseqdrop — Видаляє елемент зі стовпця типу послідовності за допомогою OID.

### Опис

```methodsynopsis
cubrid_seq_drop(    resource $conn_identifier,    string $oid,    string $attr_name,    int $index): bool
```

Функція **cubridseqdrop()** використовується для видалення елемента, який ви запитуєте з атрибута типу послідовності в базі даних.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, з яким ви хочете працювати.

`attr_name`

Ім'я атрибута, з якого ви бажаєте видалити елемент.

`index`

Індекс елемента, який потрібно видалити (починаючи з 1).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridseqdrop()****

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

cubrid_seq_drop($conn, $oid, "c", 4);

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
array(3) {
  [0]=>
  string(2) "11"
  [1]=>
  string(2) "22"
  [2]=>
  string(2) "33"
}
```

### Дивіться також

-   [cubridseqinsert()](function.cubrid-seq-insert.md) - Вставляє елемент у стовпець типу послідовності, використовуючи OID
-   [cubridseqput()](function.cubrid-seq-put.md) - Оновлює значення елемента стовпця типу послідовності за допомогою OID
