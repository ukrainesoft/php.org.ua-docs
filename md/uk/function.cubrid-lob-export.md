---
navigation:
  - function.cubrid-lob-close.md: « cubridlobclose
  - function.cubrid-lob-get.md: cubridlobget »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridлобexport
---
# cubridлобexport

(PECL CUBRID >= 8.3.1)

cubridлобexport — Експортує дані BLOB/CLOB у файл

### Опис

```methodsynopsis
cubrid_lob_export(resource $conn_identifier, resource $lob_identifier, string $path_name): bool
```

**cubridлобexport()** використовується для отримання даних BLOB/CLOB з бази даних CUBRID та збереження їхнього вмісту у файл. Щоб використати цю функцію, необхідно спочатку використати [cubridlobget()](function.cubrid-lob-get.md), щоб отримати інформацію BLOB/CLOB із CUBRID.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення.

`lob_identifier`

Ідентифікатор LOB.

`path_name`

Ім'я шляху файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridлобexport()****

```php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");
echo "Размер документа: ".cubrid_lob_size($lobs[0])." байтов";
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubridlobget()](function.cubrid-lob-get.md) - Отримує дані BLOB/CLOB
-   [cubridlobclose()](function.cubrid-lob-close.md) - Закриває дані BLOB/CLOB
-   [cubridlobsize()](function.cubrid-lob-size.md) - Отримує розмір даних BLOB/CLOB
-   [cubridlobsend()](function.cubrid-lob-send.md) - Читає дані BLOB/CLOB та відправляє їх прямо до браузера
