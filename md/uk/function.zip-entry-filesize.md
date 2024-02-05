---
navigation:
  - function.zip-entry-compressionmethod.md: « zip\_entry\_compressionmethod
  - function.zip-entry-name.md: zip\_entry\_name »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_entry\_filesize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_entry\_filesize

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_entry\_filesize — Повертає реальний розмір файлу для дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_filesize(resource $zip_entry): int|false
```

Повертає реальний розмір заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.md)

### Значення, що повертаються

Реальний розмір дескриптора директорії або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zip\_open()](function.zip-open.md) \- Відкриває ZIP-архів
-   [zip\_read()](function.zip-read.md) \- Зчитує наступний запис у ZIP-архіві
