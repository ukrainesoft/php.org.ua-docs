---
navigation:
  - function.cubrid-current-oid.md: « cubridcurrentoid
  - function.cubrid-drop.md: cubriddrop »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubriddisconnect
---
# cubriddisconnect

(PECL CUBRID >= 8.3.0)

cubriddisconnect — Закриває з'єднання з базою даних

### Опис

```methodsynopsis
cubrid_disconnect(resource $conn_identifier = ?): bool
```

Функція **cubriddisconnect()** використовується для закриття оброблювача з'єднання та від'єднання від сервера. Якщо будь-який оброблювач запиту не буде закритий на цей момент, він буде примусово закритий. Функція аналогічна функції сумісності CUBRID MySQL [cubridclose()](function.cubrid-close.md)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubriddisconnect()****

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "connected successfully";

   $req = cubrid_execute( $con, "create table person(id int,name char(10))");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }

   $req = cubrid_execute( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubridclose()](function.cubrid-close.md) - Закриває з'єднання з базою даних
-   [cubridconnect()](function.cubrid-connect.md) - Відкриває з'єднання з сервером CUBRID
-   [cubridconnectwithurl()](function.cubrid-connect-with-url.md) - Створює оточення для з'єднання із сервером CUBRID
