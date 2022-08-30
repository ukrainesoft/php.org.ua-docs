Повертає набір прав для поточного елемента DirectoryIterator item

-   [« DirectoryIterator::getPathname](directoryiterator.getpathname.md)
    
-   [DirectoryIterator::getSize »](directoryiterator.getsize.md)
    
-   [PHP Manual](index.md)
    
-   [DirectoryIterator](class.directoryiterator.md)
    
-   Повертає набір прав для поточного елемента DirectoryIterator item
    

# DirectoryIterator::getPerms

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getPerms — Повертає набір прав для поточного елемента DirectoryIterator item

### Опис

```methodsynopsis
public DirectoryIterator::getPerms(): int
```

Повертає набір прав для поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає набір прав для поточного файлу як десяткового числа int.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getPerms()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if (!$fileinfo->isDot()) {
        $octal_perms = substr(sprintf('%o', $fileinfo->getPerms()), -4);
        echo $fileinfo->getFilename() . " " . $octal_perms . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg 0644
banana.jpg 0644
index.php 0744
pear.jpg 0644
```

### Дивіться також

-   [DirectoryIterator::isExecutable()](directoryiterator.isexecutable.md) - Визначає, чи поточний елемент DirectoryIterator виконується
-   [DirectoryIterator::isReadable()](directoryiterator.isreadable.md) - Визначає, чи доступний поточний елемент DirectoryIterator для читання
-   [DirectoryIterator::isWritable()](directoryiterator.iswritable.md) - Визначає, чи доступний поточний елемент DirectoryIterator для запису