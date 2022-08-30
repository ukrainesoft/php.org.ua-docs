Переміщення покажчика на початок

-   [« FilesystemIterator::next](filesystemiterator.next.md)
    
-   [FilesystemIterator::setFlags »](filesystemiterator.setflags.md)
    
-   [PHP Manual](index.md)
    
-   [FilesystemIterator](class.filesystemiterator.md)
    
-   Переміщення покажчика на початок
    

# FilesystemIterator::rewind

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::rewind — Переміщення покажчика на початок

### Опис

```methodsynopsis
public FilesystemIterator::rewind(): void
```

Перекладає покажчик початку директорії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **FilesystemIterator::rewind()****

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);

echo $iterator->key() . "\n";

$iterator->next();
echo $iterator->key() . "\n";

$iterator->rewind();
echo $iterator->key() . "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg
banana.jpg
apple.jpg
```

### Дивіться також

-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) - Встановлює покажчик на перший елемент DirectoryIterator