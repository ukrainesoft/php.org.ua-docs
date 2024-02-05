---
navigation:
  - function.zip-open.md: « zip\_open
  - book.zlib.md: Zlib »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_read

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_read — Зчитує наступний запис у ZIP-архіві

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_read(resource $zip): resource|false
```

Зчитує наступний запис у ZIP-архіві.

### Список параметрів

`zip`

ZIP-файл, попередньо відкритий за допомогою функції [zip\_open()](function.zip-open.md)

### Значення, що повертаються

Повертає запис каталогу для подальшого використання з функціями `zip_entry_...`, или\*\*`false`\*\*якщо більше немає записів для читання, або код помилки, якщо вона відбулася.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zip\_open()](function.zip-open.md) \- Відкриває ZIP-архів
-   [zip\_close()](function.zip-close.md) \- Закриває дескриптор ZIP-архіву
-   [zip\_entry\_open()](function.zip-entry-open.md) \- відкриває директорію для читання
-   [zip\_entry\_read()](function.zip-entry-read.md) \- Читає дані із відкритого раніше дескриптора директорії
