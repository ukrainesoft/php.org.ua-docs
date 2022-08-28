Повернути поточну позицію файлового покажчика

-   [« SplFileObject::fstat](splfileobject.fstat.html)
    
-   [SplFileObject::ftruncate »](splfileobject.ftruncate.html)
    
-   [PHP Manual](index.html)
    
-   [SplFileObject](class.splfileobject.html)
    
-   Повернути поточну позицію файлового покажчика
    

# SplFileObject::ftell

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplFileObject::ftell — Повернути поточну позицію файлового покажчика

### Опис

```methodsynopsis
public SplFileObject::ftell(): int|false
```

Повертає поточну позицію файлового покажчика, яка представляє поточне усунення у файловому потоці.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає позицію файлового покажчика у вигляді цілого чи числа **`false`** у разі помилки.

### Приклади

**Приклад #1 Приклад використання **SplFileObject::ftell()****

```php
<?php
$file = new SplFileObject("/etc/passwd");

// Читаем первую строку
$data = $file->fgets();

// Определяем, где мы?
echo $file->ftell();
?>
```

### Дивіться також

-   [ftell()](function.ftell.html) - Повертає поточну позицію покажчика читання/запису файлу