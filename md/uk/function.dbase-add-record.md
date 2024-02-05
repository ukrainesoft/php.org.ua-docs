---
navigation:
  - ref.dbase.md: « dBase
  - function.dbase-close.md: dbase\_close »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_add\_record
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_add\_record

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_add\_record — Додає запис до бази даних

### Опис

```methodsynopsis
dbase_add_record(resource $database, array $data): bool
```

Додає дані до бази даних

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

`data`

Індексований масив із даними. Кількість елементів має дорівнювати числу полів у базі даних, в іншому випадку **dbase\_add\_record()** не вдасться виконати.

> **Зауваження** :
> 
> Якщо ви використовуєте як параметр запис, який повернула функція [dbase\_get\_record()](function.dbase-get-record.md), не забудьте сбросить ключ`deleted`(прим пер. - unset(record\['deleted'\]);

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Вставлення запису до бази даних dBase**

```php
<?php

// открыть БД в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  dbase_add_record($db, array(
      date('Ymd'),
      'Maxim Topolov',
      '23',
      'max@example.com',
      'T'));
  dbase_close($db);
}

?>
```

### Дивіться також

-   [dbase\_delete\_record()](function.dbase-delete-record.md) \- Видалення записів із бази даних
-   [dbase\_replace\_record()](function.dbase-replace-record.md) \- Замінює запис у базі даних
