---
navigation:
  - function.gzuncompress.md: « gzuncompress
  - function.inflate-add.md: inflate\_add »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzwrite
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає кількість записаних байт (без урахування стиснення) у потік gz-файлу або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `length` тепер припускає значення null; раніше значенням за умовчанням був |
| 7.4.0 | В случае возникновения ошибки функция возвращает\*\*`false`\*\*. . раніше повертався |

### Приклади

**Пример #1 Пример использования**gzwrite()\*\*\*\*

```php
<?php
$string = 'Какие-то данные для сжатия';
$gz = gzopen('somefile.gz','w9');
gzwrite($gz, $string);
gzclose($gz);
?>
```

### Дивіться також

-   [gzread()](function.gzread.md) \- Бінарне читання gz-файлу
-   [gzopen()](function.gzopen.md) \- Відкрити gz-файл
