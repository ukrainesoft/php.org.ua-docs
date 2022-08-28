Повертає метод стиснення дескриптора директорії

-   [« zip\_entry\_compressedsize](function.zip-entry-compressedsize.html)
    
-   [zip\_entry\_filesize »](function.zip-entry-filesize.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zip](ref.zip.html)
    
-   Повертає метод стиснення дескриптора директорії
    

# zipentrycompressionmethod

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentrycompressionmethod - Повертає метод стиснення дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_compressionmethod(resource $zip_entry): string|false
```

Повертає метод стиснення дескриптора директорії, заданого в `zip_entry`

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.html)

### Значення, що повертаються

Метод стиснення або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------|
|        | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.html) |

### Дивіться також

-   [zip\_open()](function.zip-open.html) - Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві