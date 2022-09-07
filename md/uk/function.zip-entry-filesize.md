---
navigation:
  - function.zip-entry-compressionmethod.md: « zipentrycompressionmethod
  - function.zip-entry-name.md: zipentryname »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipentryfilesize
---
# zipentryfilesize

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryfilesize — Повертає реальний розмір файлу для дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_filesize(resource $zip_entry): int|false
```

Повертає реальний розмір заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.md)

### Значення, що повертаються

Реальний розмір дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zipopen()](function.zip-open.md) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.md) - Зчитує наступний запис у ZIP-архіві
