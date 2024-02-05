---
navigation:
  - ref.bzip2.md: « Функції Bzip2
  - function.bzcompress.md: bzcompress »
  - index.md: PHP Manual
  - ref.bzip2.md: Функції Bzip2
title: bzclose
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bzclose

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

bzclose — Закриває файл bzip2

### Опис

```methodsynopsis
bzclose(resource $bz): bool
```

Закриває переданий покажчик файлу bzip2.

### Список параметрів

`bz`

Вказівник на файл. Має бути коректним і вказувати на файл, успішно відкритий [bzopen()](function.bzopen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [bzopen()](function.bzopen.md) \- Відкриває файл, стислий за допомогою bzip2
