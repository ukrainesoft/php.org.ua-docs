Створює новий BLOB-об'єкт для заповнення даними

-   [« ibase\_blob\_close](function.ibase-blob-close.html)
    
-   [ibase\_blob\_echo »](function.ibase-blob-echo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Створює новий BLOB-об'єкт для заповнення даними
    

# ibaseblobcreate

(PHP 5, PHP 7 < 7.4.0)

ibaseblobcreate — Створює новий BLOB-об'єкт для заповнення даними

### Опис

```methodsynopsis
ibase_blob_create(resource $link_identifier = null): resource|false
```

**ibaseblobcreate()** створює новий BLOB-об'єкт заповнення даними.

### Список параметрів

`link_identifier`

Ідентифікатор посилання на InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

### Значення, що повертаються

Повертає дескриптор BLOB-об'єкта для подальшого використання з [ibase\_blob\_add()](function.ibase-blob-add.html) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibase\_blob\_add()](function.ibase-blob-add.html) - Додає дані до новоствореного BLOB-об'єкту
-   [ibase\_blob\_cancel()](function.ibase-blob-cancel.html) - Скасує створення BLOB-об'єкта
-   [ibase\_blob\_close()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibase\_blob\_import()](function.ibase-blob-import.html) - Створює BLOB-об'єкт, копіює файл і закриває його.