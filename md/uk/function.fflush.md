Скидає буфер виводу у файл

-   [« feof](function.feof.html)
    
-   [fgetc »](function.fgetc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции файловой системы](ref.filesystem.html)
    
-   Скидає буфер виводу у файл
    

# fflush

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

fflush — Скидає буфер виводу у файл

### Опис

```methodsynopsis
fflush(resource $stream): bool
```

Ця функція здійснює скидання буферизованих даних у файл, який вказує `stream`

### Список параметрів

`stream`

Вказівник на файл повинен бути коректним і вказувати на файл, успішно відкритий функціями [fopen()](function.fopen.html) або [fsockopen()](function.fsockopen.html) (і все ще не закритий функцією [fclose()](function.fclose.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад запису файлу за допомогою **fflush()****

```php
<?php
$filename = 'bar.txt';

$file = fopen($filename, 'r+');
rewind($file);
fwrite($file, 'Foo');
fflush($file);
ftruncate($file, ftell($file));
fclose($file);
?>
```

### Дивіться також

-   [clearstatcache()](function.clearstatcache.html) - Очищує кеш стану файлів
-   [fwrite()](function.fwrite.html) - Бінарно-безпечний запис у файл