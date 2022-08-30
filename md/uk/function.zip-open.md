Відкриває ZIP-архів

-   [« zipentryread](function.zip-entry-read.html)
    
-   [zipread »](function.zip-read.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Zip](ref.zip.md)
    
-   Відкриває ZIP-архів
    

# zipopen

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipopen — Відкриває ZIP-архів

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_open(string $filename): resource|int|false
```

Відкриває ZIP-архів для читання.

### Список параметрів

`filename`

Ім'я ZIP-архіву для відкриття.

### Значення, що повертаються

Повертає посилання на ресурс для подальшого використання з функціями [zipread()](function.zip-read.html) і [zipclose()](function.zip-close.html) або повертає номер помилки, якщо `filename` не існує або у разі іншої помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::open()](ziparchive.open.md) |

### Дивіться також

-   [zipread()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві
-   [zipclose()](function.zip-close.html) - Закриває дескриптор ZIP-архіву