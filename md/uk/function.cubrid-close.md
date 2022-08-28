Закриває з'єднання з базою даних

-   [« cubrid\_client\_encoding](function.cubrid-client-encoding.html)
    
-   [cubrid\_data\_seek »](function.cubrid-data-seek.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Закриває з'єднання з базою даних
    

# cubridclose

(PECL CUBRID >= 8.3.1)

cubridclose — Закриває з'єднання з базою даних

### Опис

```methodsynopsis
cubrid_close(resource $conn_identifier = ?): bool
```

Функція **cubridclose()** використовується для закриття оброблювача з'єднання та від'єднання від сервера. Якщо будь-який оброблювач запиту не буде закритий на цей момент, він буде примусово закритий. Функція аналогічна функції CUBRID [cubrid\_disconnect()](function.cubrid-disconnect.html)

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.html) з'єднання.

### Значення, що повертаються

**`true`**, у разі успішного виконання.

**`false`**, у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridclose()****

```php
<?php
$con = cubrid_connect ("localhost", 33000, "demodb");
if ($con) {
   echo "подключение успешно выполнено";
   $req = cubrid_execute ( $con, "insert into person values(1,'James')");
   if ($req) {
      cubrid_close_request ($req);
      cubrid_commit ($con);
   } else {
      cubrid_rollback ($con);
   }
   cubrid_close ($con);
}
?>
```

### Дивіться також

-   [cubrid\_disconnect()](function.cubrid-disconnect.html) - Закриває з'єднання з базою даних
-   [cubrid\_connect()](function.cubrid-connect.html) - Відкриває з'єднання з сервером CUBRID
-   [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.html) - Створює оточення для з'єднання із сервером CUBRID