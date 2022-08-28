Отримує кількість байтів від відкритого BLOB-об'єкта

-   [« ibase\_blob\_echo](function.ibase-blob-echo.html)
    
-   [ibase\_blob\_import »](function.ibase-blob-import.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Отримує кількість байтів від відкритого BLOB-об'єкта
    

# ibaseblobget

(PHP 5, PHP 7 < 7.4.0)

ibaseblobget — Отримує кількість байтів від відкритого BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_get(resource $blob_handle, int $len): string
```

Функція повертає не більше `len` байт із BLOB-об'єкта, який був відкритий для читання за допомогою [ibase\_blob\_open()](function.ibase-blob-open.html)

> **Зауваження**
> 
> Неможливо прочитати з BLOB-об'єкта, який був відкритий для запису за допомогою [ibase\_blob\_create()](function.ibase-blob-create.html)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibase\_blob\_open()](function.ibase-blob-open.html)

`len`

Розмір даних, що повертаються.

### Значення, що повертаються

Повертає не більше `len` байт із BLOB-об'єкта або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibaseblobget()****

```php
<?php
$result    = ibase_query("SELECT blob_value FROM table");
$data      = ibase_fetch_object($result);
$blob_data = ibase_blob_info($data->BLOB_VALUE);
$blob_hndl = ibase_blob_open($data->BLOB_VALUE);
echo         ibase_blob_get($blob_hndl, $blob_data[0]);
?>
```

Хоча цей приклад робить не більше, ніж 'ibaseblobecho($data->BLOBVALUE)', він показує, як отримати інформацію в $variable для подальших маніпуляцій.

### Дивіться також

-   [ibase\_blob\_open()](function.ibase-blob-open.html) - Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibase\_blob\_close()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibase\_blob\_echo()](function.ibase-blob-echo.html) - Виводить вміст BLOB-об'єкта у браузер