---
navigation:
  - function.cubrid-set-db-parameter.md: « cubrid\_set\_db\_parameter
  - function.cubrid-set-query-timeout.md: cubrid\_set\_query\_timeout »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_set\_drop
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_set\_drop

(PECL CUBRID >= 8.3.0)

cubrid\_set\_drop — Видаляє елемент із стовпця заданого типу, використовуючи OID

### Опис

```methodsynopsis
cubrid_set_drop(    resource $conn_identifier,    string $oid,    string $attr_name,    string $set_element): bool
```

Функция**cubrid\_set\_drop()** використовується для видалення елемента, який ви запитуєте із заданого атрибута типу набору (set, multiset) бази даних.

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_set\_drop()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_set_drop($conn, $oid, "b", "1");

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
array(2) {
  [0]=>
  string(1) "2"
  [1]=>
  string(1) "3"
}
```

### Дивіться також

-   [cubrid\_set\_add()](function.cubrid-set-add.md) \- Вставляє один елемент для встановлення стовпця типу за допомогою OID
