Закриває дескриптор ZIP-архіву

-   [« Функции Zip](ref.zip.html)
    
-   [zip\_entry\_close »](function.zip-entry-close.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zip](ref.zip.html)
    
-   Закриває дескриптор ZIP-архіву
    

# zipclose

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipclose — Закриває дескриптор ZIP-архіву

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_close(resource $zip): void
```

Закриває дескриптор ZIP-архіву.

### Список параметрів

`zip`

ZIP-файл має бути відкритий за допомогою функції [zip\_open()](function.zip-open.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::close()](ziparchive.close.html) |

### Дивіться також

-   [zip\_open()](function.zip-open.html) - Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві