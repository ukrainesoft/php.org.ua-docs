---
navigation:
  - function.cubrid-close-request.md: « cubrid\_close\_request
  - function.cubrid-col-size.md: cubrid\_col\_size »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_col\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_col\_get

(PECL CUBRID >= 8.3.0)

cubrid\_col\_get — Отримання контенту стовпця типу колекція OID

### Опис

```methodsynopsis
cubrid_col_get(resource $conn_identifier, string $oid, string $attr_name): array
```

Функция**cubrid\_col\_get()** використовується отримання контенту елемента типу колекція (set, multiset, sequence) як масиву.

### Список параметрів

`conn_identifier`

Ідентифікатор колекції.

`oid`

OID екземпляра, який ви хочете прочитати.

`attr_name`

Ім'я атрибута ви хочете прочитати.

### Значення, що повертаються

Індексований масив (починається з 0), що містить запитані елементи у разі успіху.

**`false`** (для помилки від ситуації, коли атрибут містить порожню колекцію або NULL, у разі виникнення помилки буде викликано попередження; у цьому випадку потрібно використовувати функцію [cubrid\_error\_code()](function.cubrid-error-code.md)), у разі невдачі.

### Приклади

**Приклад #1 Приклад використання** cubrid\_col\_get()\*\*\*\*

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
