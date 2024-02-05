---
navigation:
  - function.cubrid-col-get.md: « cubrid\_col\_get
  - function.cubrid-column-names.md: cubrid\_column\_names »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_col\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_col\_size

(PECL CUBRID >= 8.3.0)

cubrid\_col\_size — Отримує кількість елементів у стовпці типу колекція OID

### Опис

```methodsynopsis
cubrid_col_size(resource $conn_identifier, string $oid, string $attr_name): int
```

Функция**cubrid\_col\_size()** використовується для отримання кількості елементів в атрибуті типу колекції (set, multiset, sequence).

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`oid`

OID екземпляра.

`attr_name`

Назва атрибута, з яким ви хочете працювати.

### Значення, що повертаються

Кількість елементів, у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.1 | Змінено значення, що повертається: у разі невдачі повертається **`false`**, а чи не -1. |

### Приклади

**Пример #1 Пример использования**cubrid\_col\_size()\*\*\*\*

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

$size = cubrid_col_size($conn, $oid, "b");
var_dump($size);

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
int(3)
```
