---
navigation:
  - function.cubrid-lob2-export.md: « cubrid\_lob2\_export
  - function.cubrid-lob2-new.md: cubrid\_lob2\_new »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_import
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_import

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_import — Імпортує дані BLOB/CLOB із файлу

### Опис

```methodsynopsis
cubrid_lob2_import(resource $lob_identifier, string $file_name): bool
```

Функция**cubrid\_lob2\_import()** використовується для збереження вмісту BLOB/CLOB з файлу. Щоб використовувати цю функцію, потрібно використовувати [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або спочатку отримати LOB-об'єкт із бази даних CUBRID. Якщо файл існує, операція завершиться помилкою. Функція не впливатиме на положення курсору LOB-об'єкта. Вона керує всім LOB-об'єктом.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, отриманий у результаті [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

`filename`

Ім'я файлу, до якого ви хочете імпортувати дані BLOB/CLOB. Також підтримується шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования[cubrid\_lob2\_export()](function.cubrid-lob2-export.md)**

```php
<?php

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");
cubrid_bind($req, 1, 1);

$lob = cubrid_lob2_new($conn, "clob");
cubrid_lob2_import($lob, "doc_1.txt");
cubrid_lob2_bind($req, 2, $lob, 'CLOB'); // или cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_lob2_close($lob);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) \- Створює об'єкт LOB
-   [cubrid\_lob2\_close()](function.cubrid-lob2-close.md) \- Закриває об'єкт LOB
-   [cubrid\_lob2\_export()](function.cubrid-lob2-export.md) \- Експортує LOB-об'єкт у файл
-   [cubrid\_lob2\_bind()](function.cubrid-lob2-bind.md) \- Зв'язує об'єкт LOB або рядок у вигляді об'єкта LOB з підготовленим оператором як параметри
