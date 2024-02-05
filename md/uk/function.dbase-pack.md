---
navigation:
  - function.dbase-open.md: « dbase\_open
  - function.dbase-replace-record.md: dbase\_replace\_record »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_pack
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_pack

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_pack - Фіксує видалення з бази даних

### Опис

```methodsynopsis
dbase_pack(resource $database): bool
```

Фіксує видалення з бази даних, остаточно видаляє записи, які були позначені видалення за допомогою [dbase\_delete\_record()](function.dbase-delete-record.md). . Зверніть увагу, що після виконання цієї операції файл буде усічений (на відміну від команди dBASE III's PACK)

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Очищення бази даних dBase**

```php
<?php

// открываем в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      dbase_delete_record($db, $i);
  }
  // стираем базу
  dbase_pack($db);
}

?>
```

### Дивіться також

-   [dbase\_delete\_record()](function.dbase-delete-record.md) \- Видалення записів із бази даних
