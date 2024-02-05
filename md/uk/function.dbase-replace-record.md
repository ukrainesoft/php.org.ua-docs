---
navigation:
  - function.dbase-pack.md: « dbase\_pack
  - book.ibase.md: Firebird/InterBase »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_replace\_record
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_replace\_record

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_replace\_record — Замінює запис у базі даних

### Опис

```methodsynopsis
dbase_replace_record(resource $database, array $data, int $number): bool
```

Замінює цей запис у базі даних на задані значення.

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

`data`

Індексований масив даних. Кількість елементів має дорівнювати кількості полів у базі даних, в іншому випадку виклик **dbase\_replace\_record()** не вдастся.

> **Зауваження** :
> 
> Якщо ви використовуєте як параметр запис, який повернув [dbase\_get\_record()](function.dbase-get-record.md), не забудьте сбросить ключ с именем`deleted`

`number`

Ціле число, яке може бути в діапазоні від 1 до числа записів у базі даних (яка повернула функція [dbase\_numrecords()](function.dbase-numrecords.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Оновлення запису в базі даних**

```php
<?php

// откроем в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  // получим старую запись
  $row = dbase_get_record_with_names($db, 1);

  // сбросим пометку 'deleted'
  unset($row['deleted']);

  // Установим в поле даты текущую дату
  $row['date'] = date('Ymd');

  // Преобразуем $row в массив
  $row = array_values($row);

  // Заменим запись
  dbase_replace_record($db, $row, 1);
  dbase_close($db);
}

?>
```

### Примітки

> **Зауваження** :
> 
> При использовании[dbase\_get\_record()](function.dbase-get-record.md) і [dbase\_get\_record\_with\_names()](function.dbase-get-record-with-names.md), поля логічного типу повертаються як ціле (int) значення ( либо ). Якщо ви збираєтеся записувати ці значення назад, потрібно пам'ятати, що результат стане рівним

### Дивіться також

-   [dbase\_add\_record()](function.dbase-add-record.md) \- Додає запис до бази даних
-   [dbase\_delete\_record()](function.dbase-delete-record.md) \- Видалення записів із бази даних
