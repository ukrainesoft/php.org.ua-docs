---
navigation:
  - function.zip-close.md: « zip\_close
  - function.zip-entry-compressedsize.md: zip\_entry\_compressedsize »
  - index.md: PHP Manual
  - ref.zip.md: Функції Zip
title: zip\_entry\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# zip\_entry\_close

(PHP 4 >= 4.1.0, PHP 5 >= 5.2.0, PHP 7, PHP 8, PECL zip >= 1.0.0)

zip\_entry\_close - Закриває дескриптор директорії

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
zip_entry_close(resource $zip_entry): bool
```

Закриває заданий дескриптор директорії.

### Список параметрів

`zip_entry`

Дескриптор директорії, раніше відкритий функцією [zip\_entry\_open()](function.zip-entry-open.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла на користь Object API. |

### Дивіться також

-   [zip\_entry\_open()](function.zip-entry-open.md) \- відкриває директорію для читання
-   [zip\_entry\_read()](function.zip-entry-read.md) \- Читає дані із відкритого раніше дескриптора директорії
