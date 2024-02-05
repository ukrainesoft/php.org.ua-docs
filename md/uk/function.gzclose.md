---
navigation:
  - function.deflate-init.md: « deflate\_init
  - function.gzcompress.md: gzcompress »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzclose
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gzclose()\*\*\*\*

```php
<?php
$gz = gzopen('somefile.gz','w9');
gzputs ($gz, 'Добавлено в файл somefile.gz');
gzclose($gz);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
