---
navigation:
  - function.deflate-init.html: « deflateinit
  - function.gzcompress.html: gzcompress »
  - index.html: PHP Manual
  - ref.zlib.html: Функции Zlib
title: gzclose
---
# gzclose

(PHP 4, PHP 5, PHP 7, PHP 8)

gzclose — Закрити покажчик відкритого gz-файлу

### Опис

```methodsynopsis
gzclose(resource $stream): bool
```

Закриває відкритий gz-файл за переданим покажчиком.

### Список параметрів

`stream`

Вказівник на файл gz. Повинен вказувати на файл, успішно відкритий [gzopen()](function.gzopen.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gzclose()****

```php
<?php
$gz = gzopen('somefile.gz','w9');
gzputs ($gz, 'Добавлено в файл somefile.gz');
gzclose($gz);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
