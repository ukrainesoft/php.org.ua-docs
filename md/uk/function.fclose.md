Закриває відкритий дескриптор файлу

-   [« diskfreespace](function.diskfreespace.html)
    
-   [fdatasync »](function.fdatasync.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Закриває відкритий дескриптор файлу
    

# fclose

(PHP 4, PHP 5, PHP 7, PHP 8)

fclose — Закриває відкритий дескриптор файлу

### Опис

```methodsynopsis
fclose(resource $stream): bool
```

Функція закриває файл, який вказує дескриптор `stream`

### Список параметрів

`stream`

Дескриптор повинен бути коректним та вказувати на файл, відкритий раніше за допомогою функції [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Простий приклад використання функції **fclose()****

```php
<?php

$handle = fopen('somefile.txt', 'r');

fclose($handle);

?>
```

### Дивіться також

-   [fopen()](function.fopen.html) - Відкриває файл або URL
-   [fsockopen()](function.fsockopen.html) - Відкриває з'єднання з інтернет-сокетом або доменним сокетом Unix