Повертає inode поточного елемента DirectoryIterator

-   [« DirectoryIterator::getGroup](directoryiterator.getgroup.html)
    
-   [DirectoryIterator::getMTime »](directoryiterator.getmtime.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає inode поточного елемента DirectoryIterator
    

# DirectoryIterator::getInode

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getInode — Повертає inode поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getInode(): int
```

Повертає inode поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає файл inode.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getInode()****

Приклад виведе inode директорії, що містить скрипт, що виконується.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
echo $iterator->getInode();
?>
```

### Дивіться також

-   [DirectoryIterator::getGroup()](directoryiterator.getgroup.html) - Повертає ідентифікатор групи поточного елемента DirectoryIterator
-   [DirectoryIterator::getOwner()](directoryiterator.getowner.html) - Повертає ідентифікатор власника поточного елемента DirectoryIterator
-   [DirectoryIterator::getPerms()](directoryiterator.getperms.html) - Повертає набір прав для поточного елемента DirectoryIterator item
-   [fileinode()](function.fileinode.html) - Повертає індексний дескриптор файлу