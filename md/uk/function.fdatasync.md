---
navigation:
  - function.fclose.md: « fclose
  - function.feof.md: feof »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fdatasync
---
# fdatasync

(PHP 8> = 8.1.0)

fdatasync — Синхронізує дані (але не метадані) з файлом

### Опис

```methodsynopsis
fdatasync(resource $stream): bool
```

Функція синхронізує вміст `stream` з накопичувачем, як і [fsync()](function.fsync.md), але не синхронізує метадані файлу. Варто звернути увагу, що ця функція фактично відрізняється лише у системах POSIX. У Windows вона є псевдонімом [fsync()](function.fsync.md)

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **fdatasync()****

```php
<?php

$file = 'test.txt';

$stream = fopen($file, 'w');
fwrite($stream, 'тестовые данные');
fwrite($stream, "\r\n");
fwrite($stream, 'дополнительные данные');

fdatasync($stream);
fclose($stream);
?>
```

### Дивіться також

-   [fflush()](function.fflush.md) - скидає буфер виведення у файл
-   [fsync()](function.fsync.md) - Синхронізує зміни у файлі (включаючи метадані)
