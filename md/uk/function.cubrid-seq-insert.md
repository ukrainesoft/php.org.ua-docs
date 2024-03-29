---
navigation:
  - function.cubrid-seq-drop.md: « cubrid\_seq\_drop
  - function.cubrid-seq-put.md: cubrid\_seq\_put »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_seq\_insert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_seq\_insert

(PECL CUBRID >= 8.3.0)

cubrid\_seq\_insert — Вставляє елемент у стовпець типу послідовності за допомогою OID

### Опис

```methodsynopsis
cubrid_seq_insert(    resource $conn_identifier,    string $oid,    string $attr_name,    int $index,    string $seq_element): bool
```

Функция**cubrid\_col\_insert()** використовується для вставлення елемента в атрибут типу послідовності у запрошеному місці.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра, з яким ви хочете працювати.

`attr_name`

Ім'я атрибута, до якого ви хочете вставити екземпляр.

`index`

Розташування елемента, який ви хочете вставити елемент (починаючи з 1).

`seq_element`

Вміст елемента, який потрібно вставити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_seq\_insert()\*\*\*\*

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

cubrid_seq_insert($conn, $oid, "c", 5, "44");

$attr = cubrid_col_get($conn, $oid, "c");
var_dump($attr);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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
array(5) {
  [0]=>
  string(2) "11"
  [1]=>
  string(2) "22"
  [2]=>
  string(2) "33"
  [3]=>
  string(3) "333"
  [4]=>
  string(2) "44"
}
```

### Дивіться також

-   [cubrid\_seq\_drop()](function.cubrid-seq-drop.md) \- Видаляє елемент зі стовпця типу послідовності, використовуючи OID
-   [cubrid\_seq\_put()](function.cubrid-seq-put.md) \- Оновлює значення елемента стовпця типу послідовності за допомогою OID
