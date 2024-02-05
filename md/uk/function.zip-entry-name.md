---
navigation:
  - function.zip-entry-filesize.md: « zip\_entry\_filesize
  - function.zip-entry-open.md: zip\_entry\_open »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_entry\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_entry\_name

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_entry\_name — Отримує ім'я дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_name(resource $zip_entry): string|false
```

Повертає ім'я заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.md)

### Значення, що повертаються

Ім'я дескриптора директорії або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zip\_open()](function.zip-open.md) \- Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.md) \- Зчитує наступний запис у ZIP-архіві
