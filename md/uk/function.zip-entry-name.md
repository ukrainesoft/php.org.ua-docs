Отримує ім'я дескриптора директорії

-   [« zipentryfilesize](function.zip-entry-filesize.html)
    
-   [zipentryopen »](function.zip-entry-open.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Zip](ref.zip.md)
    
-   Отримує ім'я дескриптора директорії
    

# zipentryname

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryname — Отримує ім'я дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_name(resource $zip_entry): string|false
```

Повертає ім'я заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.html)

### Значення, що повертаються

Ім'я дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                             |
|--------|------------------------------------------------------------------------------------------------------|
|        | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zipopen()](function.zip-open.html) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві