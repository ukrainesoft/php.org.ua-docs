Скасує створення BLOB

-   [« fbirdblobadd](function.fbird-blob-add.html)
    
-   [fbirdblobclose »](function.fbird-blob-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Скасує створення BLOB
    

# fbirdblobcancel

(PHP 5, PHP 7 < 7.4.0)

fbirdblobcancel — Скасовує створення BLOB

### Опис

```methodsynopsis
fbird_blob_cancel(resource $blob_handle): bool
```

Ця функція припиняє використання BLOB, якщо вона ще не була закрита [fbirdblobclose()](function.fbird-blob-close.html)

### Список параметрів

`blob_handle`

Дескриптор BLOB, відкритий за допомогою [fbirdblobcreate()](function.fbird-blob-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fbirdblobclose()](function.fbird-blob-close.html) - Псевдонім ibaseblobclose
-   [fbirdblobcreate()](function.fbird-blob-create.html) - Псевдонім ibaseblobcreate
-   [fbirdblobimport()](function.fbird-blob-import.html) - Псевдонім ibaseblobimport