Повертає шлях до поточного елементу DirectoryIterator без імені файлу

-   [« DirectoryIterator::getOwner](directoryiterator.getowner.html)
    
-   [DirectoryIterator::getPathname »](directoryiterator.getpathname.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає шлях до поточного елементу DirectoryIterator без імені файлу
    

# DirectoryIterator::getPath

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getPath — Повертає шлях до поточного елемента DirectoryIterator без імені файлу

### Опис

```methodsynopsis
public DirectoryIterator::getPath(): string
```

Повертає шлях до поточного елементу [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до файлу (без імені файлу та завершального слішу).

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getPath()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
echo $iterator->getPath();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/examples/public_html
```

### Дивіться також

-   [DirectoryIterator::getBasename()](directoryiterator.getbasename.html) - Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator
-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.html) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getPathname()](directoryiterator.getpathname.html) - Повертає шлях та ім'я файлу поточного елемента DirectoryIterator
-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу