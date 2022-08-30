Повертає ідентифікатор власника поточного елемента DirectoryIterator

-   [« DirectoryIterator::getMTime](directoryiterator.getmtime.html)
    
-   [DirectoryIterator::getPath »](directoryiterator.getpath.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ідентифікатор власника поточного елемента DirectoryIterator
    

# DirectoryIterator::getOwner

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getOwner — Повертає ідентифікатор власника поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getOwner(): int
```

Повертає ідентифікатор власника поточного елемента [DirectoryIterator](class.directoryiterator.html) у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Власник файлу у числовому форматі.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getOwner()****

Приклад показує власника директорії, що містить скрипт, що виконується.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
print_r(posix_getpwuid($iterator->getOwner()));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [name] => tom
    [passwd] => x
    [uid] => 501
    [gid] => 42
    [gecos] => Tom Cat
    [dir] => /home/tom
    [shell] => /bin/bash
)
```

### Дивіться також

-   [DirectoryIterator::getGroup()](directoryiterator.getgroup.html) - Повертає ідентифікатор групи поточного елемента DirectoryIterator
-   [DirectoryIterator::getiNode()](directoryiterator.getinode.html) - Повертає inode поточного елемента DirectoryIterator
-   [DirectoryIterator::getPerms()](directoryiterator.getperms.html) - Повертає набір прав для поточного елемента DirectoryIterator item
-   [posixgetpwuid()](function.posix-getpwuid.html) - Повертає інформацію про користувача, використовуючи його ID