Зчитує наступний запис у ZIP-архіві

-   [« zip\_open](function.zip-open.html)
    
-   [Zlib »](book.zlib.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zip](ref.zip.html)
    
-   Зчитує наступний запис у ZIP-архіві
    

# zipread

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipread — Зчитує наступний запис у ZIP-архіві

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_read(resource $zip): resource|false
```

Зчитує наступний запис у ZIP-архіві.

### Список параметрів

`zip`

ZIP-файл, попередньо відкритий за допомогою функції [zip\_open()](function.zip-open.html)

### Значення, що повертаються

Повертає запис каталогу для подальшого використання з функціями `zip_entry_...`, або **`false`**якщо більше немає записів для читання, або код помилки, якщо вона відбулася.

### список змін

| Версия | Описание                                                                                               |
|--------|--------------------------------------------------------------------------------------------------------|
|        | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.html) |

### Дивіться також

-   [zip\_open()](function.zip-open.html) - Відкриває ZIP-архів
-   [zip\_close()](function.zip-close.html) - Закриває дескриптор ZIP-архіву
-   [zip\_entry\_open()](function.zip-entry-open.html) - відкриває директорію для читання
-   [zip\_entry\_read()](function.zip-entry-read.html) - Читає дані із відкритого раніше дескриптора директорії