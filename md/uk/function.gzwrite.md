---
navigation:
  - function.gzuncompress.html: « gzuncompress
  - function.inflate-add.html: inflateadd »
  - index.html: PHP Manual
  - ref.zlib.html: Функции Zlib
title: gzwrite
---
# gzwrite

(PHP 4, PHP 5, PHP 7, PHP 8)

gzwrite — Бінарний запис до gz-файлу

### Опис

```methodsynopsis
gzwrite(resource $stream, string $data, ?int $length = null): int|false
```

**gzwrite()** записує вміст `data` у цей gz-файл.

### Список параметрів

`stream`

Вказівник на gz-файл, повернутий після його успішного відкриття функцією [gzopen()](function.gzopen.md)

`data`

Рядок, що записується.

`length`

Число стиснених байтів для запису. Якщо зазначено, операція завершиться після запису `length` (до стиснення) байт або при досягненні кінця рядка, залежно від того, що настане раніше . `data`

### Значення, що повертаються

Повертає кількість записаних байт (без урахування стиснення) у потік gz-файлу або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер припускає значення null; раніше значенням за умовчанням був `0` |
|  | У разі помилки функція повертає **`false`**. раніше повертався `0` |

### Приклади

**Приклад #1 Приклад використання **gzwrite()****

```php
<?php
$string = 'Какие-то данные для сжатия';
$gz = gzopen('somefile.gz','w9');
gzwrite($gz, $string);
gzclose($gz);
?>
```

### Дивіться також

-   [gzread()](function.gzread.md) - Бінарне читання gz-файлу
-   [gzopen()](function.gzopen.md) - Відкрити gz-файл
