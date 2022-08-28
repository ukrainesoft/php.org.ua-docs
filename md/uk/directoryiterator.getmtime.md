Повертає час останньої зміни поточного елементу DirectoryIterator

-   [« DirectoryIterator::getInode](directoryiterator.getinode.html)
    
-   [DirectoryIterator::getOwner »](directoryiterator.getowner.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає час останньої зміни поточного елементу DirectoryIterator
    

# DirectoryIterator::getMTime

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getMTime — Повертає час останньої зміни поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getMTime(): int
```

Повертає час останньої зміни поточного елемента [DirectoryIterator](class.directoryiterator.html) у форматі позначки часу Unix.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Час останньої зміни файлу у форматі відмітки Unix.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getMTime()****

Приклад виведе список файлів директорії, що містить скрипт і час їх останньої модифікації.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . " " . $fileinfo->getMTime() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg 1240047118
banana.jpg 1240065176
index.php 1240047208
pear.jpg 12240047979
```

### Дивіться також

-   [DirectoryIterator::getATime()](directoryiterator.getatime.html) - Повертає час останнього доступу до поточного елементу DirectoryIterator
-   [DirectoryIterator::getCTime()](directoryiterator.getctime.html) - Повертає час останньої зміни inode поточного елемента DirectoryIterator
-   [filemtime()](function.filemtime.html) - Повертає час останньої зміни файлу