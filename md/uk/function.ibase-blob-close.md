Закриває BLOB-об'єкт

-   [« ibase\_blob\_cancel](function.ibase-blob-cancel.html)
    
-   [ibase\_blob\_create »](function.ibase-blob-create.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Закриває BLOB-об'єкт
    

# ibaseblobclose

(PHP 5, PHP 7 < 7.4.0)

ibaseblobclose — Закриває BLOB-об'єкт

### Опис

```methodsynopsis
ibase_blob_close(resource $blob_handle): mixed
```

Ця функція закриває BLOB-об'єкт, відкритий для читання за допомогою [ibase\_blob\_open()](function.ibase-blob-open.html) або [ibase\_blob\_create()](function.ibase-blob-create.html)

### Список параметрів

`blob_handle`

BLOB-об'єкт, відкритий за допомогою [ibase\_blob\_create()](function.ibase-blob-create.html) або [ibase\_blob\_open()](function.ibase-blob-open.html)

### Значення, що повертаються

Якщо BLOB-об'єкт читався, функція повертає **`true`** у разі успішного виконання, якщо BLOB записувався, функція повертає рядок, що містить ідентифікатор BLOB-об'єкта, призначений їй базою даних. У разі невдачі функція повертає **`false`**

### Дивіться також

-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.html) - Скасує створення BLOB-об'єкта
-   [ibase\_blob\_open()](function.ibase-blob-open.html) - Відкриває BLOB-об'єкт для вилучення частин даних