---
navigation:
  - function.cubrid-client-encoding.md: « cubrid\_client\_encoding
  - function.cubrid-data-seek.md: cubrid\_data\_seek »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_close

(PECL CUBRID >= 8.3.1)

cubrid\_close — Закриває з'єднання з базою даних

### Опис

```methodsynopsis
cubrid_close(resource $conn_identifier = ?): bool
```

Функция**cubrid\_close()** використовується для закриття оброблювача з'єднання та від'єднання від сервера. Якщо будь-який оброблювач запиту не буде закритий на цей момент, він буде примусово закритий. Функція аналогічна функції CUBRID [cubrid\_disconnect()](function.cubrid-disconnect.md)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.md)соединение.

### Значення, що повертаються

**`true`**, у разі успішного виконання.

**`false`**, у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_close()\*\*\*\*

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "подключение успешно выполнено";
   $req = cubrid_execute ( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_close ($con);
}
?>
```

### Дивіться також

-   [cubrid\_disconnect()](function.cubrid-disconnect.md) \- Закриває з'єднання з базою даних
-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) \- Створює оточення для з'єднання із сервером CUBRID
