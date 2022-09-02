---
navigation:
  - function.zip-entry-open.md: « zipentryopen
  - function.zip-open.md: zipopen »
  - index.md: PHP Manual
  - ref.zip.md: Функции Zip
title: zipentryread
---
# zipentryread

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zipentryread - Читає дані з відкритого раніше дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_read(resource $zip_entry, int $len = 1024): string|false
```

Читає дані із відкритого раніше дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zipread()](function.zip-read.md)

`len`

Число байт, яке потрібно рахувати.

> **Зауваження**
> 
> У параметрі необхідно вказувати обсяг даних, які ви хочете рахувати, без урахування стиснення.

### Значення, що повертаються

Повертає лічені дані, порожній рядок, якщо досягнуто кінець файлу, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла на користь Object API, дивіться [ZipArchive::getFromIndex()](ziparchive.getfromindex.md) |

### Дивіться також

-   [zipentryopen()](function.zip-entry-open.md) - відкриває директорію для читання
-   [zipentryclose()](function.zip-entry-close.md) - закриває дескриптор директорії
-   [zipentryfilesize()](function.zip-entry-filesize.md) - Повертає реальний розмір файлу для дескриптора директорії
