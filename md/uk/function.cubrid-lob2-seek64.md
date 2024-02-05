---
navigation:
  - function.cubrid-lob2-read.md: « cubrid\_lob2\_read
  - function.cubrid-lob2-seek.md: cubrid\_lob2\_seek »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob2\_seek64
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob2\_seek64

(PECL CUBRID >= 8.4.1)

cubrid\_lob2\_seek64 - Переміщує курсор LOB-об'єкта

### Опис

```methodsynopsis
cubrid_lob2_seek64(resource $lob_identifier, string $offset, int $origin = CUBRID_CURSOR_CURRENT): bool
```

Функция**cubrid\_lob2\_seek64()** використовується для переміщення позиції курсора LOB-об'єкта на значення, задане у параметрі `offset`, в направлении, заданном в параметре`origin`Если значение параметра`offset` більше, ніж можна зберегти цілі дані, ви можете використовувати цю функцію.

Щоб встановити параметр `origin`, Ви можете використовувати **`CUBRID_CURSOR_FIRST`**, щоб встановити позицію курсора, що переміщається вперед `offset` одиниць від початку LOB-об'єкта. У цьому випадку параметр `offset` має бути позитивним значенням.

Якщо ви використовуєте \*\*`CUBRID_CURSOR_CURRENT`\*\*для`origin`, Ви можете рухатися вперед або назад, `offset` може бути позитивним чи негативним.

Якщо ви використовуєте \*\*`CUBRID_CURSOR_LAST`\*\*для`origin`Ви можете переміщати назад на одиницю `offset` з кінця LOB-об'єкта. У цьому випадку параметр `offset` має бути позитивним значенням.

> **Зауваження** :
> 
> Якщо ви використовуєте цю функцію для переміщення позиції курсора LOB-об'єкта, ви повинні передати `offset` як рядок.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB внаслідок роботи функції [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або отриманий із набору результатів.

`offset`

Кількість одиниць, яку потрібно перемістити курсор.

`origin`

Параметр може мати такі значення:

CUBRID\_CURSOR\_FIRST: рухатись вперед від початку LOB-об'єкта.

CUBRID\_CURSOR\_CURRENT: рухатись вперед або назад від поточної позиції.

CUBRID\_CURSOR\_LAST: рухатись назад з кінця LOB-об'єкта.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования:**cubrid\_lob2\_seek64()****

```php
<?php
// test_lob (id INT, contents CLOB)
// Длина данных doc_1.txt должна быть больше 20101029056306120215.

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

$req = cubrid_execute($conn, "select * from test_lob");
$row = cubrid_fetch_row($req, CUBRID_LOB);
$lob = $row[1];

cubrid_lob2_seek64($lob, "20101029056306120215", CUBRID_CURSOR_FIRST);
$data = cubrid_lob2_read($lob, 20);
echo $data."\n";
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob2\_read()](function.cubrid-lob2-read.md) \- Здійснює читання з даних BLOB/CLOB
-   [cubrid\_lob2\_write()](function.cubrid-lob2-write.md) \- Записує до LOB-об'єкту
-   [cubrid\_lob2\_seek()](function.cubrid-lob2-seek.md) \- Переміщує курсор LOB-об'єкта
-   [cubrid\_lob2\_tell()](function.cubrid-lob2-tell.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_tell64()](function.cubrid-lob2-tell64.md) \- Повідомляє положення курсору LOB-об'єкта
-   [cubrid\_lob2\_size()](function.cubrid-lob2-size.md) \- Отримує розмір LOB-об'єкта
-   [cubrid\_lob2\_size64()](function.cubrid-lob2-size64.md) \- Отримує розмір LOB-об'єкта
