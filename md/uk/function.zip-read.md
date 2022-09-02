---
navigation:
  - function.zip-open.md: « zipopen
  - book.zlib.md: Zlib »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipread
---
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

ZIP-файл, попередньо відкритий за допомогою функції [zipopen()](function.zip-open.md)

### Значення, що повертаються

Повертає запис каталогу для подальшого використання з функціями `zip_entry_...`, або \*\*`false`\*\*якщо більше немає записів для читання, або код помилки, якщо вона відбулася.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zipopen()](function.zip-open.md) - Відкриває ZIP-архів
-   [zipclose()](function.zip-close.md) - Закриває дескриптор ZIP-архіву
-   [zipentryopen()](function.zip-entry-open.md) - відкриває директорію для читання
-   [zipentryread()](function.zip-entry-read.md) - Читає дані із відкритого раніше дескриптора директорії
