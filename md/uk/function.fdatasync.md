Синхронізує дані (але не метадані) з файлом

-   [« fclose](function.fclose.html)
    
-   [feof »](function.feof.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Синхронізує дані (але не метадані) з файлом
    

# fdatasync

(PHP 8> = 8.1.0)

fdatasync — Синхронізує дані (але не метадані) з файлом

### Опис

```methodsynopsis
fdatasync(resource $stream): bool
```

Функція синхронізує вміст `stream` з накопичувачем, як і [fsync()](function.fsync.html), але не синхронізує метадані файлу. Варто звернути увагу, що ця функція фактично відрізняється лише у системах POSIX. У Windows вона є псевдонімом [fsync()](function.fsync.html)

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

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

-   [fflush()](function.fflush.html) - скидає буфер виведення у файл
-   [fsync()](function.fsync.html) - Синхронізує зміни у файлі (включаючи метадані)