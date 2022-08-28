Закриває дескриптор директорії

-   [« zip\_close](function.zip-close.html)
    
-   [zip\_entry\_compressedsize »](function.zip-entry-compressedsize.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zip](ref.zip.html)
    
-   Закриває дескриптор директорії
    

# zipentryclose

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryclose - Закриває дескриптор директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_close(resource $zip_entry): bool
```

Закриває заданий дескриптор директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, раніше відкритий функцією [zip\_entry\_open()](function.zip-entry-open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API. |

### Дивіться також

-   [zip\_entry\_open()](function.zip-entry-open.html) - відкриває директорію для читання
-   [zip\_entry\_read()](function.zip-entry-read.html) - Читає дані із відкритого раніше дескриптора директорії