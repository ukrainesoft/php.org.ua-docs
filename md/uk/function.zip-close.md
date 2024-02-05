---
navigation:
  - ref.zip.md: « Функції Zip
  - function.zip-entry-close.md: zip\_entry\_close »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_close

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_close — Закриває дескриптор ZIP-архіву

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_close(resource $zip): void
```

Закриває дескриптор ZIP-архіву.

### Список параметрів

`zip`

ZIP-файл має бути відкритий за допомогою функції [zip\_open()](function.zip-open.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::close()](ziparchive.close.md) |

### Дивіться також

-   [zip\_open()](function.zip-open.md) \- Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.md) \- Зчитує наступний запис у ZIP-архіві
