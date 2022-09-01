---
navigation:
  - function.zip-entry-filesize.html: « zipentryfilesize
  - function.zip-entry-open.html: zipentryopen »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipentryname
---
# zipentryname

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryname — Отримує ім'я дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_name(resource $zip_entry): string|false
```

Повертає ім'я заданого дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.md)

### Значення, що повертаються

Ім'я дескриптора директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::statIndex()](ziparchive.statindex.md) |

### Дивіться також

-   [zipopen()](function.zip-open.md) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.md) - Зчитує наступний запис у ZIP-архіві
