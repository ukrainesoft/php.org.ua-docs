Додає дані до новоствореного BLOB-об'єкту

-   [« ibase\_backup](function.ibase-backup.html)
    
-   [ibase\_blob\_cancel »](function.ibase-blob-cancel.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Додає дані до новоствореного BLOB-об'єкту
    

# ibaseblobadd

(PHP 5, PHP 7 < 7.4.0)

ibaseblobadd — Додає дані до новоствореного BLOB-об'єкта

### Опис

```methodsynopsis
ibase_blob_add(resource $blob_handle, string $data): void
```

**ibaseblobadd()** додає дані в BLOB-об'єкт, створений за допомогою [ibase\_blob\_create()](function.ibase-blob-create.html)

### Список параметрів

`blob_handle`

Дескриптор BLOB-об'єкта, відкритого за допомогою [ibase\_blob\_create()](function.ibase-blob-create.html)

`data`

Дані для додавання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.html) - Скасує створення BLOB-об'єкта
-   [ibase\_blob\_close()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibase\_blob\_create()](function.ibase-blob-create.html) - Створює новий BLOB-об'єкт для заповнення даними
-   [ibase\_blob\_import()](function.ibase-blob-import.html) - Створює BLOB-об'єкт, копіює файл і закриває його.