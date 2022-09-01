---
navigation:
  - function.cubrid-lob-get.html: « cubridlobget
  - function.cubrid-lob-size.html: cubridlobsize »
  - index.html: PHP Manual
  - ref.cubrid.html: Функции CUBRID
title: cubridлобsend
---
# cubridлобsend

(PECL CUBRID >= 8.3.1)

cubridлобsend — Читає дані BLOB/CLOB і надсилає їх прямо до браузера

### Опис

```methodsynopsis
cubrid_lob_send(resource $conn_identifier, resource $lob_identifier): bool
```

**cubridлобsend()** зчитує дані BLOB/CLOB і передає їх у браузер. Щоб використати цю функцію, необхідно спочатку використати [cubridlobget()](function.cubrid-lob-get.html), щоб отримати інформацію BLOB/CLOB із CUBRID.

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

-   [cubridlobget()](function.cubrid-lob-get.html) - Отримує дані BLOB/CLOB
-   [cubridlobclose()](function.cubrid-lob-close.html) - Закриває дані BLOB/CLOB
-   [cubridlobsize()](function.cubrid-lob-size.html) - Отримує розмір даних BLOB/CLOB
-   [cubridlobexport()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл
