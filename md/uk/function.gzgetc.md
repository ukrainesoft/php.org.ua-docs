---
navigation:
  - function.gzfile.md: « gzfile
  - function.gzgets.md: gzgets »
  - index.md: PHP Manual
  - ref.zlib.md: Функции Zlib
title: gzgetc
---
# gzgetc

(PHP 4, PHP 5, PHP 7, PHP 8)

gzgetc — Отримати символ із покажчика на gz-файл

### Опис

```methodsynopsis
gzgetc(resource $stream): string|false
```

Повертає рядок, що містить один символ (несжатий), зчитаний із заданого покажчика gz-файлу.

### Список параметрів

`stream`

Вказівник на файл gz. Він має бути коректним і повинен вказувати на файл, успішно відкритий. [gzopen()](function.gzopen.md)

### Значення, що повертаються

Символ (несжатий) або **`false`** у випадку EOF (на відміну від [gzeof()](function.gzeof.md)

### Приклади

**Приклад #1 Приклад використання **gzgetc()****

```php
<?php
$gz = gzopen('somefile.gz', 'r');
while (!gzeof($gz)) {
  echo gzgetc($gz);
}
gzclose($gz);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
-   [gzgets()](function.gzgets.md) - Отримати рядок із покажчика файлу
