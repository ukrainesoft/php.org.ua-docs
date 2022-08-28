Читає дані BLOB/CLOB та відправляє їх прямо до браузера

-   [« cubrid\_lob\_get](function.cubrid-lob-get.html)
    
-   [cubrid\_lob\_size »](function.cubrid-lob-size.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Читає дані BLOB/CLOB та відправляє їх прямо до браузера
    

# cubridлобsend

(PECL CUBRID >= 8.3.1)

cubridлобsend — Читає дані BLOB/CLOB і надсилає їх прямо до браузера

### Опис

```methodsynopsis
cubrid_lob_send(resource $conn_identifier, resource $lob_identifier): bool
```

**cubridлобsend()** зчитує дані BLOB/CLOB і передає їх у браузер. Щоб використати цю функцію, необхідно спочатку використати [cubrid\_lob\_get()](function.cubrid-lob-get.html), щоб отримати інформацію BLOB/CLOB із CUBRID.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення.

`lob_identifier`

Ідентифікатор LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridлобsend()****

```php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");

cubrid_lob_send($conn, $lobs[0]);
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob\_get()](function.cubrid-lob-get.html) - Отримує дані BLOB/CLOB
-   [cubrid\_lob\_close()](function.cubrid-lob-close.html) - Закриває дані BLOB/CLOB
-   [cubrid\_lob\_size()](function.cubrid-lob-size.html) - Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл