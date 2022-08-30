Скасує створення BLOB-об'єкта

-   [« ibaseblobadd](function.ibase-blob-add.html)
    
-   [ibaseblobclose »](function.ibase-blob-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Скасує створення BLOB-об'єкта
    

# ibaseblobcancel

(PHP 5, PHP 7 < 7.4.0)

ibaseblobcancel — Скасує створення об'єкта BLOB

### Опис

```methodsynopsis
ibase_blob_cancel(resource $blob_handle): bool
```

Ця функція відкидає BLOB-об'єкт, якщо його ще не було закрито за допомогою [ibaseblobclose()](function.ibase-blob-close.html)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритий за допомогою [ibaseblobcreate()](function.ibase-blob-create.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobclose()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibaseblobcreate()](function.ibase-blob-create.html) - Створює новий BLOB-об'єкт для заповнення даними
-   [ibaseblobimport()](function.ibase-blob-import.html) - Створює BLOB-об'єкт, копіює файл і закриває його.