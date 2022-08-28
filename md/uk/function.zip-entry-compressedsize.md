Повертає стислий розмір файлу для дескриптора директорії

-   [« zip\_entry\_close](function.zip-entry-close.html)
    
-   [zip\_entry\_compressionmethod »](function.zip-entry-compressionmethod.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zip](ref.zip.html)
    
-   Повертає стислий розмір файлу для дескриптора директорії
    

# zipentrycompressedsize

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentrycompressedsize — Повертає стислий розмір файлу для дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_compressedsize(resource $zip_entry): int|false
```

Повертає стислий розмір заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.html)

### Значення, що повертаються

Стиснутий розмір дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.html) |

### Дивіться також

-   [zip\_open()](function.zip-open.html) - Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві