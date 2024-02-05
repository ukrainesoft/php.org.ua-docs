---
navigation:
  - function.cubrid-current-oid.md: « cubrid\_current\_oid
  - function.cubrid-drop.md: cubrid\_drop »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_disconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_disconnect

(PECL CUBRID >= 8.3.0)

cubrid\_disconnect — Закриває з'єднання з базою даних

### Опис

```methodsynopsis
cubrid_disconnect(resource $conn_identifier = ?): bool
```

Функция**cubrid\_disconnect()** використовується для закриття оброблювача з'єднання та від'єднання від сервера. Якщо будь-який оброблювач запиту не буде закритий на цей момент, він буде примусово закритий. Функція аналогічна функції сумісності CUBRID MySQL [cubrid\_close()](function.cubrid-close.md)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_disconnect()\*\*\*\*

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "connected successfully";

   $req = cubrid_execute( $con, "create table person(id int,name char(10))");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }

   $req = cubrid_execute( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request($req);
      cubrid_commit($con);
   } else {
      cubrid_rollback($con);
   }
   cubrid_disconnect($con);
}
?>
```

### Дивіться також

-   [cubrid\_close()](function.cubrid-close.md) \- Закриває з'єднання з базою даних
-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) \- Створює оточення для з'єднання із сервером CUBRID
