---
navigation:
  - function.fstat.html: « fstat
  - function.ftell.html: ftell »
  - index.html: PHP Manual
  - ref.filesystem.html: Функції файлової системи
title: fsync
---
# fsync

(PHP 8> = 8.1.0)

fsync — Синхронізує зміни у файлі (включаючи метадані)

### Опис

```methodsynopsis
fsync(resource $stream): bool
```

Функція синхронізує зміни у файлі, включаючи метадані. Вона схожа на [fflush()](function.fflush.html), але також дає інструкції операційній системі про запис на накопичувач.

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **fsync()****

```php
<?php

$file = 'test.txt';

$stream = fopen($file, 'w');
fwrite($stream, 'тестовые данные');
fwrite($stream, "\r\n");
fwrite($stream, 'дополнительные данные');

fsync($stream);
fclose($stream);
?>
```

### Дивіться також

-   [fdatasync()](function.fdatasync.html) - Синхронізує дані (але не метадані) із файлом
-   [fflush()](function.fflush.html) - скидає буфер виведення у файл
