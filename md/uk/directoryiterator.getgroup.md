Повертає ідентифікатор групи поточного елемента DirectoryIterator

-   [« DirectoryIterator::getFilename](directoryiterator.getfilename.html)
    
-   [DirectoryIterator::getInode »](directoryiterator.getinode.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ідентифікатор групи поточного елемента DirectoryIterator
    

# DirectoryIterator::getGroup

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getGroup — Повертає ідентифікатор групи поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getGroup(): int
```

Повертає ідентифікатор групи поточного файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор групи поточного елемента [DirectoryIterator](class.directoryiterator.html) у числовому форматі.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getGroup()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
$groupid  = $iterator->getGroup();
echo 'Директория принадлежит группе ' . $groupid . "\n";
print_r(posix_getgrgid($groupid));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Директория принадлежит группе 42
Array
(
    [name]    => toons
    [passwd]  => x
    [members] => Array
        (
            [0] => tom
            [1] => jerry
        )
    [gid]     => 42
)
```

### Дивіться також

-   [DirectoryIterator::getiNode()](directoryiterator.getinode.html) - Повертає inode поточного елемента DirectoryIterator
-   [DirectoryIterator::getOwner()](directoryiterator.getowner.html) - Повертає ідентифікатор власника поточного елемента DirectoryIterator
-   [DirectoryIterator::getPerms()](directoryiterator.getperms.html) - Повертає набір прав для поточного елемента DirectoryIterator item
-   [filegroup()](function.filegroup.html) - Отримує ідентифікатор групи файлу
-   [posixgetgrgid()](function.posix-getgrgid.html) - Повертає інформацію про групу за її ID