---
navigation:
  - function.gzencode.md: « gzencode
  - function.gzfile.md: gzfile »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzeof
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzeof

(PHP 4, PHP 5, PHP 7, PHP 8)

gzeof — Перевіряє, чи знаходиться поточна позиція в кінці (EOF) gz-файлу

### Опис

```methodsynopsis
gzeof(resource $stream): bool
```

Перевіряє, чи відповідає позиція покажчика GZ-файлі позиції EOF (end-of-file, кінець файлу).

### Список параметрів

`stream`

Вказівник на файл gz. Він має бути коректним і повинен вказувати на файл, успішно відкритий. [gzopen()](function.gzopen.md)

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо позиція покажчика gz-файлу відповідає EOF або виникає помилка; інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання** gzeof()\*\*\*\*

```php
<?php
$gz = gzopen('somefile.gz', 'r');
while (!gzeof($gz)) {
  echo gzgetc($gz);
}
gzclose($gz);
?>
```
