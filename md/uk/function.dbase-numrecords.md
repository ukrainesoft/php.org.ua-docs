---
navigation:
  - function.dbase-numfields.md: « dbase\_numfields
  - function.dbase-open.md: dbase\_open »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_numrecords
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_numrecords

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_numrecords — Отримує кількість записів у базі даних

### Опис

```methodsynopsis
dbase_numrecords(resource $database): int
```

Отримує кількість записів (рядків) у зазначеній базі даних.

> **Зауваження** :
> 
> Записи, позначені як віддалені, також враховуються.

> **Зауваження** :
> 
> Записи бази даних нумеруються від 1 `dbase_numrecords($db)`, тогда как поля от 0 до`dbase_numfields($db)-1`

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

### Значення, що повертаються

Кількість записів у базі даних, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Цикл з усіх записів бази даних**

```php
<?php

// открываем в режиме для чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      //выполнение каких-либо действий с записью
  }
}

?>
```

### Дивіться також

-   [dbase\_numfields()](function.dbase-numfields.md) \- Отримує кількість полів бази даних
