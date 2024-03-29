---
navigation:
  - function.gzeof.md: « gzeof
  - function.gzgetc.md: gzgetc »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzfile
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzfile

(PHP 4, PHP 5, PHP 7, PHP 8)

gzfile — Зчитує весь gz-файл у масив

### Опис

```methodsynopsis
gzfile(string $filename, int $use_include_path = 0): array|false
```

Аналогична[readgzfile()](function.readgzfile.md), За винятком того, що вона повертає файл у масиві.

### Список параметрів

`filename`

Ім'я файлу.

`use_include_path`

Якщо ви хочете, щоб також перевірялася наявність файлу в директоріях [include\_path](ini.core.md#ini.include-path), встановіть значення цього параметра в

### Значення, що повертаються

Масив рядків файлу, у кожному елементі масиву знаходиться один рядок, порожні рядки включаються, а перенесення рядків, як і раніше, додаються або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** gzfile()\*\*\*\*

```php
<?php
$lines = gzfile('somefile.gz');
foreach ($lines as $line) {
    echo $line;
}
?>
```

### Дивіться також

-   [readgzfile()](function.readgzfile.md) \- Виводить вміст gz-файлу
-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
