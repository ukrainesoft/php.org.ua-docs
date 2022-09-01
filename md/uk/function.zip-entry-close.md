---
navigation:
  - function.zip-close.html: « zipclose
  - function.zip-entry-compressedsize.html: zipentrycompressedsize »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipentryclose
---
# zipentryclose

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryclose - Закриває дескриптор директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_close(resource $zip_entry): bool
```

Закриває заданий дескриптор директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, раніше відкритий функцією [zipentryopen()](function.zip-entry-open.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API. |

### Дивіться також

-   [zipentryopen()](function.zip-entry-open.html) - відкриває директорію для читання
-   [zipentryread()](function.zip-entry-read.html) - Читає дані із відкритого раніше дескриптора директорії
