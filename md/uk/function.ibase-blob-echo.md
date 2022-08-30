Виводить вміст BLOB-об'єкта у браузер

-   [« ibaseblobcreate](function.ibase-blob-create.html)
    
-   [ibaseblobget »](function.ibase-blob-get.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Виводить вміст BLOB-об'єкта у браузер
    

# ibaseblobecho

(PHP 5, PHP 7 < 7.4.0)

ibaseblobecho — Виводить вміст BLOB-об'єкта у браузер

### Опис

```methodsynopsis
ibase_blob_echo(string $blob_id): bool
```

```methodsynopsis
ibase_blob_echo(resource $link_identifier, string $blob_id): bool
```

Функція відкриває BLOB-об'єкт для читання та надсилає його вміст на стандартний висновок (у більшості випадків – браузер).

### Список параметрів

`link_identifier`

Ідентифікатор посилання InterBase. Якщо не вказано, передбачається останнє відкрите посилання.

`blob_id`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseblobopen()](function.ibase-blob-open.html) - Відкриває BLOB-об'єкт для вилучення частин даних
-   [ibaseblobclose()](function.ibase-blob-close.html) - Закриває BLOB-об'єкт
-   [ibaseblobget()](function.ibase-blob-get.html) - Отримує кількість байтів від відкритого BLOB-об'єкта