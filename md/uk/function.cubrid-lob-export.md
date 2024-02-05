---
navigation:
  - function.cubrid-lob-close.md: « cubrid\_lob\_close
  - function.cubrid-lob-get.md: cubrid\_lob\_get »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob\_export
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob\_export

(PECL CUBRID >= 8.3.1)

cubrid\_lob\_export — Експортує дані BLOB/CLOB у файл

### Опис

```methodsynopsis
cubrid_lob_export(resource $conn_identifier, resource $lob_identifier, string $path_name): bool
```

**cubrid\_lob\_export()** використовується для отримання даних BLOB/CLOB з бази даних CUBRID та збереження їхнього вмісту у файл. Щоб використати цю функцію, необхідно спочатку використати [cubrid\_lob\_get()](function.cubrid-lob-get.md), щоб отримати інформацію BLOB/CLOB із CUBRID.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`lob_identifier`

Ідентифікатор LOB.

`path_name`

Ім'я шляху файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_lob\_export()\*\*\*\*

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

-   [cubrid\_lob\_get()](function.cubrid-lob-get.md) \- Отримує дані BLOB/CLOB
-   [cubrid\_lob\_close()](function.cubrid-lob-close.md) \- Закриває дані BLOB/CLOB
-   [cubrid\_lob\_size()](function.cubrid-lob-size.md) \- Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob\_send()](function.cubrid-lob-send.md) \- Читає дані BLOB/CLOB та відправляє їх прямо до браузера
