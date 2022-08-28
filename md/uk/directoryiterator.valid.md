Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом

-   [« DirectoryIterator::\_\_toString](directoryiterator.tostring.html)
    
-   [EmptyIterator »](class.emptyiterator.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
    

# DirectoryIterator::valid

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::valid — Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом

### Опис

```methodsynopsis
public DirectoryIterator::valid(): bool
```

Перевіряє, чи є поточний елемент [DirectoryIterator](class.directoryiterator.html) допустимим файлом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**якщо елемент є допустимим, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::valid()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

// Цикл до конца итератора
while($iterator->valid()) {
    $iterator->next();
}

$iterator->valid(); // FALSE
$iterator->rewind();
$iterator->valid(); // TRUE

?>
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.html) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.html) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.html) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::rewind()](directoryiterator.rewind.html) - Встановлює покажчик на перший елемент DirectoryIterator
-   [Iterator::valid()](iterator.valid.html) - Перевіряє коректність поточної позиції