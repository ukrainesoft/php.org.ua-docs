---
navigation:
  - function.cubrid-lob2-tell.md: « cubrid\_lob2\_tell
  - function.cubrid-lock-read.md: cubrid\_lock\_read »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_write
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_write

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_write - Записує в LOB-об'єкт

### Опис

```methodsynopsis
cubrid_lob2_write(resource $lob_identifier, string $buf): bool
```

Функция**cubrid\_lob2\_write()** зчитує дані з `buf` та зберігає їх у LOB-об'єкт. Зауважте, що функція може лише додавати символи.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, отриманий у результаті [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

`buf`

Дані, які потрібно записати в LOB-об'єкт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_lob2\_write()\*\*\*\*

```php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(2, ?)");

$lob = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob, "Hello world");

cubrid_lob2_bind($req, 1, $lob);
cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

**Приклад #2 Приклад використання** cubrid\_lob2\_write()\*\*\*\*

```php
<?php
// test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(1, ?)");
$lob1 = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob1, "cubrid php driver");
cubrid_lob2_bind($req, 1, $lob1);
cubrid_execute($req);

$req = cubrid_execute($conn, "select * from test_lob");

$row = cubrid_fetch_row($req, CUBRID_LOB);
$lob2 = $row[1];
cubrid_lob2_seek($lob2, 0, CUBRID_CURSOR_LAST);

$pos = cubrid_lob2_tell($lob2);
print "позиция перед записью: $pos\n";

cubrid_lob2_write($lob2, "Hello world");

$pos = cubrid_lob2_tell($lob2);
print "позиция после записи: $pos\n";

cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob2\_read()](function.cubrid-lob2-read.md) \- Здійснює читання з даних BLOB/CLOB
-   [cubrid\_lob2\_seek()](function.cubrid-lob2-seek.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_seek64()](function.cubrid-lob2-seek64.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_tell()](function.cubrid-lob2-tell.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_tell64()](function.cubrid-lob2-tell64.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_size()](function.cubrid-lob2-size.md) \- Отримує розмір LOB-об'єкта
-   [cubrid\_lob2\_size64()](function.cubrid-lob2-size64.md) \- Отримує розмір LOB-об'єкта
