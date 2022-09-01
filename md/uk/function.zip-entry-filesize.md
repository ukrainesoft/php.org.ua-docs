---
navigation:
  - function.zip-entry-compressionmethod.html: « zipentrycompressionmethod
  - function.zip-entry-name.html: zipentryname »
  - index.html: PHP Manual
  - ref.zip.html: Функции Zip
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

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.html)

### Значення, що повертаються

Реальний розмір дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.html) |

### Дивіться також

-   [zipopen()](function.zip-open.html) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.html) - Зчитує наступний запис у ZIP-архіві
