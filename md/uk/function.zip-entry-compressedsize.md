Повертає стислий розмір файлу для дескриптора директорії

-   [« zipentryclose](function.zip-entry-close.html)
    
-   [zipentrycompressionmethod »](function.zip-entry-compressionmethod.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Zip](ref.zip.md)
    
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

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.html)

### Значення, що повертаються

Стиснутий розмір дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zipopen()](function.zip-open.html) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві