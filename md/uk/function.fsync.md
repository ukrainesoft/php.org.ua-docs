---
navigation:
  - function.fstat.md: « fstat
  - function.ftell.md: ftell »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: fsync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fsync

(PHP 8 >= 8.1.0)

fsync — Синхронізує зміни у файлі (включаючи метадані)

### Опис

```methodsynopsis
fsync(resource $stream): bool
```

Функція синхронізує зміни у файлі, включаючи метадані. Вона схожа на [fflush()](function.fflush.md), але також дає інструкції операційній системі про запис на накопичувач.

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.md) або [fsockopen()](function.fsockopen.md) (і все ще не закритий функцією [fclose()](function.fclose.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**fsync()\*\*\*\*

```php
<?php

$file = 'test.txt';

$stream = fopen($file, 'w');
fwrite($stream, 'тестовые данные');
fwrite($stream, "\r\n");
fwrite($stream, 'дополнительные данные');

fsync($stream);
fclose($stream);
?>
```

### Дивіться також

-   [fdatasync()](function.fdatasync.md) \- Синхронізує дані (але не метадані) із файлом
-   [fflush()](function.fflush.md) \- скидає буфер виведення у файл
