---
navigation:
  - function.zip-entry-read.md: « zip\_entry\_read
  - function.zip-read.md: zip\_read »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_open

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_open — Відкриває ZIP-архів

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

Повертає посилання на ресурс для подальшого використання з функціями [zip\_read()](function.zip-read.md) і [zip\_close()](function.zip-close.md) або повертає номер помилки, якщо `filename` не існує або у разі іншої помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::open()](ziparchive.open.md) |

### Дивіться також

-   [zip\_read()](function.zip-read.md) \- Зчитує наступний запис у ZIP-архіві
-   [zip\_close()](function.zip-close.md) \- Закриває дескриптор ZIP-архіву
