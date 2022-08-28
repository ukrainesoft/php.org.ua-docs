Закриває базу даних

-   [« dbase\_add\_record](function.dbase-add-record.html)
    
-   [dbase\_create »](function.dbase-create.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Закриває базу даних
    

# dbaseclose

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbaseclose — Закриває базу даних

### Опис

```methodsynopsis
dbase_close(resource $database): bool
```

Закриває вказаний ресурс бази даних.

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.html) або [dbase\_create()](function.dbase-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Закриття файлу бази даних dBase**

```php
<?php

// открыть БД в режиме чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  // получить некоторые данные

  dbase_close($db);
}

?>
```

### Дивіться також

-   [dbase\_open()](function.dbase-open.html) - Відкриває базу даних
-   [dbase\_create()](function.dbase-create.html) - Створює базу даних