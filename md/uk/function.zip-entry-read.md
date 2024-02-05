---
navigation:
  - function.zip-entry-open.md: « zip\_entry\_open
  - function.zip-open.md: zip\_open »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_entry\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_entry\_read

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_entry\_read - Читає дані з відкритого раніше дескриптора директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_read(resource $zip_entry, int $len = 1024): string|false
```

Читає дані із відкритого раніше дескриптора директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, що повертається функцією [zip\_read()](function.zip-read.md)

`len`

Число байт, яке потрібно рахувати.

> **Зауваження** :
> 
> У параметрі необхідно вказувати обсяг даних, які ви хочете рахувати, без урахування стиснення.

### Значення, що повертаються

Повертає лічені дані, порожній рядок, якщо досягнуто кінець файлу, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API, дивіться [ZipArchive::getFromIndex()](ziparchive.getfromindex.md) |

### Дивіться також

-   [zip\_entry\_open()](function.zip-entry-open.md) \- відкриває директорію для читання
-   [zip\_entry\_close()](function.zip-entry-close.md) \- закриває дескриптор директорії
-   [zip\_entry\_filesize()](function.zip-entry-filesize.md) \- Повертає реальний розмір файлу для дескриптора директорії
