Встановлює покажчик на перший елемент DirectoryIterator

-   [« DirectoryIterator::next](directoryiterator.next.html)
    
-   [DirectoryIterator::seek »](directoryiterator.seek.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Встановлює покажчик на перший елемент DirectoryIterator
    

# DirectoryIterator::rewind

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::rewind — Встановлює вказівник на перший елемент DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::rewind(): void
```

Встановлює вказівник на перший елемент [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::rewind()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));

$iterator->next();
echo $iterator->key(); //1

$iterator->rewind(); //переход к началу
echo $iterator->key(); //0
?>
```

### Дивіться також

-   [DirectoryIterator::current()](directoryiterator.current.html) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::key()](directoryiterator.key.html) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::next()](directoryiterator.next.html) - Переміщує покажчик на наступний елемент DirectoryIterator
-   [DirectoryIterator::valid()](directoryiterator.valid.html) - Перевіряє, чи є поточний елемент DirectoryIterator допустимим файлом
-   [Iterator::rewind()](iterator.rewind.html) – Повертає ітератор на перший елемент