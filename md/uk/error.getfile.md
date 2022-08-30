Отримує файл, у якому сталася помилка

-   [« Error::getCode](error.getcode.md)
    
-   [Error::getLine »](error.getline.md)
    
-   [PHP Manual](index.md)
    
-   [Error](class.error.md)
    
-   Отримує файл, у якому сталася помилка
    

# Error::getFile

(PHP 7, PHP 8)

Error::getFile — Отримує файл, у якому сталася помилка

### Опис

```methodsynopsis
final public Error::getFile(): string
```

Отримати ім'я файлу, в якому виникла помилка.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу, в якому виникла помилка.

### Приклади

**Приклад #1 Приклад використання **Error::getFile()****

```php
<?php
try {
    throw new Error;
} catch(Error $e) {
    echo $e->getFile();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/bjori/tmp/ex.php
```

### Дивіться також

-   [Throwable::getFile()](throwable.getfile.md) - Повертає файл, у якому викинуто виняток