Відкриває BLOB-об'єкт для вилучення частин даних

-   [« ibaseblobinfo](function.ibase-blob-info.html)
    
-   [ibaseclose »](function.ibase-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Відкриває BLOB-об'єкт для вилучення частин даних
    

# ibaseblobopen

(PHP 5, PHP 7 < 7.4.0)

ibaseblobopen — Відкриває BLOB-об'єкт для вилучення частин даних

### Опис

```methodsynopsis
ibase_blob_open(resource $link_identifier, string $blob_id): resource|false
```

```methodsynopsis
ibase_blob_open(string $blob_id): resource|false
```

Відкриває існуючий об'єкт BLOB для читання.

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

Ідентифікатор об'єкта BLOB.

### Значення, що повертаються

Повертає дескриптор BLOB-об'єкта для подальшого використання за допомогою [ibaseblobget()](function.ibase-blob-get.html) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobclose()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibaseblobecho()](function.ibase-blob-echo.html) - Виводить вміст BLOB-об'єкта у браузер
-   [ibaseblobget()](function.ibase-blob-get.html) - Отримує кількість байтів від відкритого BLOB-об'єкта