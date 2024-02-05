---
navigation:
  - function.cubrid-lob-get.md: « cubrid\_lob\_get
  - function.cubrid-lob-size.md: cubrid\_lob\_size »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob\_send
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob\_send

(PECL CUBRID >= 8.3.1)

cubrid\_lob\_send — Читає дані BLOB/CLOB і надсилає їх прямо до браузера

### Опис

```methodsynopsis
cubrid_lob_send(resource $conn_identifier, resource $lob_identifier): bool
```

**cubrid\_lob\_send()** зчитує дані BLOB/CLOB і передає їх у браузер. Щоб використати цю функцію, необхідно спочатку використати [cubrid\_lob\_get()](function.cubrid-lob-get.md), щоб отримати інформацію BLOB/CLOB із CUBRID.

### Список параметрів

`conn_identifier`

Ідентифікатор з'єднання.

`lob_identifier`

Ідентифікатор LOB.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_lob\_send()\*\*\*\*

```php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");

cubrid_lob_send($conn, $lobs[0]);
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob\_get()](function.cubrid-lob-get.md) \- Отримує дані BLOB/CLOB
-   [cubrid\_lob\_close()](function.cubrid-lob-close.md) \- Закриває дані BLOB/CLOB
-   [cubrid\_lob\_size()](function.cubrid-lob-size.md) \- Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.md) \- Експортує дані BLOB/CLOB у файл
