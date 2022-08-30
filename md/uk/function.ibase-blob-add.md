Додає дані до новоствореного BLOB-об'єкту

-   [« ibasebackup](function.ibase-backup.html)
    
-   [ibaseblobcancel »](function.ibase-blob-cancel.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
-   Додає дані до новоствореного BLOB-об'єкту
    

# ibaseblobadd

(PHP 5, PHP 7 < 7.4.0)

ibaseblobadd — Додає дані до новоствореного BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_add(resource $blob_handle, string $data): void
```

**ibaseblobadd()** додає дані в BLOB-об'єкт, створений за допомогою [ibaseblobcreate()](function.ibase-blob-create.html)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритого за допомогою [ibaseblobcreate()](function.ibase-blob-create.html)

`data`

Дані для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ibaseblobcancel()](function.ibase-blob-cancel.html) - Скасує створення BLOB-об'єкта
-   [ibaseblobclose()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibaseblobcreate()](function.ibase-blob-create.html) - Створює новий BLOB-об'єкт для заповнення даними
-   [ibaseblobimport()](function.ibase-blob-import.html) - Створює BLOB-об'єкт, копіює файл і закриває його.