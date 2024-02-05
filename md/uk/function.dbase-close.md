---
navigation:
  - function.dbase-add-record.md: « dbase\_add\_record
  - function.dbase-create.md: dbase\_create »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_close

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_close — Закриває базу даних

### Опис

```methodsynopsis
dbase_close(resource $database): bool
```

Закриває вказаний ресурс бази даних.

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

**Приклад #1 Закриття файлу бази даних dBase**

```php
<?php

// открыть БД в режиме чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  // получить некоторые данные

  dbase_close($db);
}

?>
```

### Дивіться також

-   [dbase\_open()](function.dbase-open.md) \- Відкриває базу даних
-   [dbase\_create()](function.dbase-create.md) \- Створює базу даних
