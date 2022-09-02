---
navigation:
  - ref.zip.md: « Функции Zip
  - function.zip-entry-close.md: zipentryclose »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipclose
---
# zipclose

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipclose — Закриває дескриптор ZIP-архіву

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_close(resource $zip): void
```

Закриває дескриптор ZIP-архіву.

### Список параметрів

`zip`

ZIP-файл має бути відкритий за допомогою функції [zipopen()](function.zip-open.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::close()](ziparchive.close.md) |

### Дивіться також

-   [zipopen()](function.zip-open.md) - Відкриває ZIP-архів
-   [zipread()](function.zip-read.md) - Зчитує наступний запис у ZIP-архіві
