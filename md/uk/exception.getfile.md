Отримує файл, у якому виник виняток

-   [« Exception::getCode](exception.getcode.html)
    
-   [Exception::getLine »](exception.getline.html)
    
-   [PHP Manual](index.html)
    
-   [Exception](class.exception.html)
    
-   Отримує файл, у якому виник виняток
    

# Exception::getFile

(PHP 5, PHP 7, PHP 8)

Exception::getFile — Отримує файл, у якому виник виняток

### Опис

```methodsynopsis
final public Exception::getFile(): string
```

Отримати ім'я файлу, де виняток було створено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, в якому виняток створено.

### Приклади

**Приклад #1 Приклад використання **Exception::getFile()****

```php
<?php
try {
    throw new Exception;
} catch(Exception $e) {
    echo $e->getFile();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/bjori/tmp/ex.php
```

### Дивіться також

-   [Throwable::getFile()](throwable.getfile.html) - Повертає файл, у якому викинуто виняток