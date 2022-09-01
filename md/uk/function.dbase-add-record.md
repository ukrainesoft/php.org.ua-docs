---
navigation:
  - ref.dbase.html: « dBase
  - function.dbase-close.html: dbaseclose »
  - index.html: PHP Manual
  - ref.dbase.html: dBase
title: dbaseaddrecord
---
# dbaseaddrecord

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbaseaddrecord — Додає запис до бази даних

### Опис

```methodsynopsis
dbase_add_record(resource $database, array $data): bool
```

Додає дані до бази даних

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.md)

`data`

Індексований масив із даними. Кількість елементів має дорівнювати числу полів у базі даних, в іншому випадку **dbaseaddrecord()** не вдасться виконати.

> **Зауваження**
> 
> Якщо ви використовуєте як параметр запис, який повернула функція [dbasegetrecord()](function.dbase-get-record.md), не забудьте скинути ключ `deleted`. (прим пров. - unset (record'deleted'

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Вставлення запису до бази даних dBase**

```php
<?php

// открыть БД в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  dbase_add_record($db, array(
      date('Ymd'),
      'Maxim Topolov',
      '23',
      'max@example.com',
      'T'));
  dbase_close($db);
}

?>
```

### Дивіться також

-   [dbasedeleterecord()](function.dbase-delete-record.md) - Видалення записів із бази даних
-   [dbasereplacerecord()](function.dbase-replace-record.md) - Замінює запис у базі даних
