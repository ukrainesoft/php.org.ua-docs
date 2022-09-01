---
navigation:
  - function.dbase-pack.html: « dbasepack
  - book.ibase.md: Firebird/InterBase »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbasereplacerecord
---
# dbasereplacerecord

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasereplacerecord — Замінює запис у базі даних

### Опис

```methodsynopsis
dbase_replace_record(resource $database, array $data, int $number): bool
```

Замінює цей запис у базі даних на задані значення.

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.html)

`data`

Індексований масив даних. Кількість елементів має дорівнювати кількості полів у базі даних, в іншому випадку виклик **dbasereplacerecord()** не вдастся.

> **Зауваження**
> 
> Якщо ви використовуєте як параметр запис, який повернув [dbasegetrecord()](function.dbase-get-record.html), не забудьте скинути ключ з ім'ям `deleted`

`number`

Ціле число, яке може бути в діапазоні від 1 до числа записів у базі даних (яка повернула функція [dbasenumrecords()](function.dbase-numrecords.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Оновлення запису в базі даних**

```php
<?php

// откроем в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  // получим старую запись
  $row = dbase_get_record_with_names($db, 1);

  // сбросим пометку 'deleted'
  unset($row['deleted']);

  // Установим в поле даты текущую дату
  $row['date'] = date('Ymd');

  // Преобразуем $row в Масив
  $row = array_values($row);

  // Заменим запись
  dbase_replace_record($db, $row, 1);
  dbase_close($db);
}

?>
```

### Примітки

> **Зауваження**
> 
> При використанні [dbasegetrecord()](function.dbase-get-record.html) і [dbasegetrecordwithnames()](function.dbase-get-record-with-names.html), поля логічного типу повертаються як ціле (int) значення (`0` або `1`). Якщо ви збираєтеся записувати ці значення назад, потрібно пам'ятати, що результат стане рівним `0`

### Дивіться також

-   [dbaseaddrecord()](function.dbase-add-record.html) - Додає запис до бази даних
-   [dbasedeleterecord()](function.dbase-delete-record.html) - Видалення записів із бази даних
