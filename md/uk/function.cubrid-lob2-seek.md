---
navigation:
  - function.cubrid-lob2-seek64.html: « cubridlob2seek64
  - function.cubrid-lob2-size64.html: cubridlob2size64 »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridlob2seek
---
# cubridlob2seek

(PECL CUBRID >= 8.4.1)

cubridlob2seek - Переміщує курсор LOB-об'єкта

### Опис

```methodsynopsis
cubrid_lob2_seek(resource $lob_identifier, int $offset, int $origin = CUBRID_CURSOR_CURRENT): bool
```

Функція **cubridlob2seek()** використовується для переміщення позиції курсора LOB-об'єкта на значення, задане у параметрі `offset`, у напрямку, заданому у параметрі `origin`

Щоб встановити параметр `origin`, Ви можете використовувати **`CUBRID_CURSOR_FIRST`**, щоб встановити позицію курсора, що переміщається вперед `offset` одиниць від початку LOB-об'єкта. У цьому випадку параметр `offset` має бути позитивним значенням.

Якщо ви використовуєте **`CUBRID_CURSOR_CURRENT`** для `origin`, Ви можете рухатися вперед або назад, `offset` може бути позитивним чи негативним.

Якщо ви використовуєте **`CUBRID_CURSOR_LAST`** для `origin`Ви можете переміщати назад на одиницю `offset` з кінця LOB-об'єкта. У цьому випадку параметр `offset` має бути позитивним значенням.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB внаслідок роботи функції [cubridlob2new()](function.cubrid-lob2-new.html) або отриманий із набору результатів.

`offset`

Кількість одиниць, яку потрібно перемістити курсор.

`origin`

Параметр може мати такі значення:

CUBRIDCURSORFIRST: рухатись вперед від початку LOB-об'єкта.

CUBRIDCURSORCURRENT: рухатись вперед або назад від поточної позиції.

CUBRIDCURSORLAST: рухатись назад з кінця LOB-об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridlob2seek()****

```php
<?php
// test_lob (id INT, contents CLOB)
$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");
$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES(2, ?)");

$lob = cubrid_lob2_new($conn, 'CLOB');
$len = cubrid_lob2_write($lob, "Hello world");

cubrid_lob2_seek($lob, 0, CUBRID_CURSOR_LAST);
cubrid_lob2_write($lob, "beautiful");

cubrid_lob2_seek($lob, 15, CUBRID_CURSOR_FIRST);
$data = cubrid_lob2_read($lob, 5);

echo $data."\n";

cubrid_lob2_bind($req, 1, $lob);
cubrid_execute($req);

cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubridlob2read()](function.cubrid-lob2-read.html) - Здійснює читання з даних BLOB/CLOB
-   [cubridlob2write()](function.cubrid-lob2-write.html) - Записує до LOB-об'єкту
-   [cubridlob2seek64()](function.cubrid-lob2-seek64.html) - Переміщує курсор LOB-об'єкта
-   [cubridlob2tell()](function.cubrid-lob2-tell.html) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2tell64()](function.cubrid-lob2-tell64.html) - Повідомляє положення курсору LOB-об'єкта
-   [cubridlob2size()](function.cubrid-lob2-size.html) - Отримує розмір LOB-об'єкта
-   [cubridlob2size64()](function.cubrid-lob2-size64.html) - Отримує розмір LOB-об'єкта
