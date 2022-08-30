Фіксує видалення з бази даних

-   [« dbaseopen](function.dbase-open.html)
    
-   [dbasereplacerecord »](function.dbase-replace-record.html)
    
-   [PHP Manual](index.md)
    
-   [dBase](ref.dbase.md)
    
-   Фіксує видалення з бази даних
    

# dbasepack

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasepack - Фіксує видалення з бази даних

### Опис

```methodsynopsis
dbase_pack(resource $database): bool
```

Фіксує видалення з бази даних, остаточно видаляє записи, які були позначені видалення за допомогою [dbasedeleterecord()](function.dbase-delete-record.html). Зверніть увагу, що після виконання цієї операції файл буде усічений (на відміну від команди dBASE III's PACK)

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Очищення бази даних dBase**

```php
<?php

// открываем в режиме чтения и записи
$db = dbase_open('/tmp/test.dbf', 2);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      dbase_delete_record($db, $i);
  }
  // стираем базу
  dbase_pack($db);
}

?>
```

### Дивіться також

-   [dbasedeleterecord()](function.dbase-delete-record.html) - Видалення записів із бази даних