---
navigation:
  - function.cubrid-prepare.html: « cubridprepare
  - function.cubrid-rollback.html: cubridrollback »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridput
---
# cubridput

(PECL CUBRID >= 8.3.0)

cubridput — Оновлює стовпець за допомогою OID

### Опис

```methodsynopsis
cubrid_put(    resource $conn_identifier,    string $oid,    string $attr = ?,    mixed $value): bool
```

Функція **cubridput()** використовується для оновлення атрибуту екземпляра даного `oid`

Ви можете оновити один атрибут, використовуючи рядковий тип даних для встановлення `attr`. У такому разі ви можете використовувати дані цілого числа, числа з плаваючою комою або числа рядкового типу як аргумент `value`. Щоб оновити кілька атрибутів, можна пропустити аргумент `attr` та встановити аргумент `value` у вигляді асоціативного масиву.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання

`oid`

OID екземпляра, який необхідно оновити

`attr`

Ім'я атрибута, який потрібно оновити

`value`

Нове значення, яке необхідно присвоїти атрибуту

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridput()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

@cubrid_execute($conn, "DROP TABLE foo");
cubrid_execute($conn, "CREATE TABLE foo(a int AUTO_INCREMENT, b set(int), c list(int), d char(10))");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(1, {1,2,3}, {11,22,33,333}, 'a')");
cubrid_execute($conn, "INSERT INTO foo(a, b, c, d) VALUES(2, {4,5,7}, {44,55,66,666}, 'b')");

$req = cubrid_execute($conn, "SELECT * FROM foo", CUBRID_INCLUDE_OID);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);
$oid = cubrid_current_oid($req);

$attr = cubrid_col_get($conn, $oid, "b");
var_dump($attr);

cubrid_put($conn, $oid, "b", array(2, 4, 8));

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
array(3) {
  [0]=>
  string(1) "2"
  [1]=>
  string(1) "4"
  [2]=>
  string(1) "8"
}
```

### Дивіться також

-   [cubridget()](function.cubrid-get.md) - Отримує стовпець, використовуючи OID
-   [cubridsetadd()](function.cubrid-set-add.md) - Вставляє один елемент для встановлення стовпця типу за допомогою OID
-   [cubridsetdrop()](function.cubrid-set-drop.md) - Видаляє елемент із стовпця заданого типу, використовуючи OID
-   [cubridseqinsert()](function.cubrid-seq-insert.md) - Вставляє елемент у стовпець типу послідовності, використовуючи OID
-   [cubridseqdrop()](function.cubrid-seq-drop.md) - Видаляє елемент зі стовпця типу послідовності, використовуючи OID
-   [cubridseqput()](function.cubrid-seq-put.md) - Оновлює значення елемента стовпця типу послідовності за допомогою OID
