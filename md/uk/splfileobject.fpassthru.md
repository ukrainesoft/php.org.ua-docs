Виводить весь вміст файлу, що залишився, у вихідний потік

-   [« SplFileObject::flock](splfileobject.flock.html)
    
-   [SplFileObject::fputcsv »](splfileobject.fputcsv.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Виводить весь вміст файлу, що залишився, у вихідний потік
    

# SplFileObject::fpassthru

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::fpassthru — Виводить весь вміст файлу, що залишився, у вихідний потік

### Опис

```methodsynopsis
public SplFileObject::fpassthru(): int
```

Читає дані з файлу з поточної позиції до кінця файлу та поміщає їх у буфер вихідного потоку.

Якщо ви вже записали якісь дані у файл і вам необхідно повернутися на початкову позицію, файловий покажчик можна скинути методом [SplFileObject::rewind()](splfileobject.rewind.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість символів, прочитаних із дескриптора `handle` та переданих на висновок.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::fpassthru()****

```php
<?php

// Открыть файл в режиме чтения двоичных данных
$file = new SplFileObject("./img/ok.png", "rb");

// Отправить правильные заголовки
header("Content-Type: image/png");
header("Content-Length: " . $file->getSize());

// Вывести изображение и завершить работу скрипта
$file->fpassthru();
exit;

?>
```

### Дивіться також

-   [fpassthru()](function.fpassthru.html) - Виводить всі дані з файлового покажчика, що залишилися.