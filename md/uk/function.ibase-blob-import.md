Створює BLOB-об'єкт, копіює файл і закриває його.

-   [« ibase\_blob\_get](function.ibase-blob-get.html)
    
-   [ibase\_blob\_info »](function.ibase-blob-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Створює BLOB-об'єкт, копіює файл і закриває його.
    

# ibaseblobimport

(PHP 5, PHP 7 < 7.4.0)

ibaseblobimport — Створює BLOB-об'єкт, копіює файл і закриває його.

### Опис

```methodsynopsis
ibase_blob_import(resource $link_identifier, resource $file_handle): string
```

```methodsynopsis
ibase_blob_import(resource $file_handle): string
```

Функція створює BLOB-об'єкт, зчитує весь файл, закриває його і повертає призначений ідентифікатор BLOB-об'єкта.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`file_handle`

Дескриптор файлу - функцією, що повертається. [fopen()](function.fopen.html)

### Значення, що повертаються

Повертає ідентифікатор BLOB-об'єкта у разі успішного виконання, або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibaseblobimport()****

```php
<?php
$dbh = ibase_connect($host, $username, $password);
$filename = '/tmp/bar';

$fd = fopen($filename, 'r');
if ($fd) {

    $blob = ibase_blob_import($dbh, $fd);
    fclose($fd);

    if (!is_string($blob)) {
        // импорт не удался
    } else {
        $query = "INSERT INTO foo (name, data) VALUES ('$filename', ?)";
        $prepared = ibase_prepare($dbh, $query);
        if (!ibase_execute($prepared, $blob)) {
            // запись не удалась
        }
    }
} else {
    // невозможно открыть файл данных
}
?>
```

### Дивіться також

-   [ibase\_blob\_add()](function.ibase-blob-add.html) - Додає дані до новоствореного BLOB-об'єкту
-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.html) - Скасує створення BLOB-об'єкта
-   [ibase\_blob\_close()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibase\_blob\_create()](function.ibase-blob-create.html) - Створює новий BLOB-об'єкт для заповнення даними