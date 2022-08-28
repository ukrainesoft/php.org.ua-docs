Додає запис до бази даних

-   [« dBase](ref.dbase.html)
    
-   [dbase\_close »](function.dbase-close.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Додає запис до бази даних
    

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

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.html) або [dbase\_create()](function.dbase-create.html)

`data`

Індексований масив із даними. Кількість елементів має дорівнювати числу полів у базі даних, в іншому випадку **dbaseaddrecord()** не вдасться виконати.

> **Зауваження**
> 
> Якщо ви використовуєте як параметр запис, який повернула функція [dbase\_get\_record()](function.dbase-get-record.html), не забудьте скинути ключ `deleted`. (прим пров. - unset (record'deleted'

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия      | Описание                                              |
|-------------|-------------------------------------------------------|
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

-   [dbase\_delete\_record()](function.dbase-delete-record.html) - Видалення записів із бази даних
-   [dbase\_replace\_record()](function.dbase-replace-record.html) - Замінює запис у базі даних