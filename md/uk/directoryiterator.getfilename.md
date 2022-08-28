Повертає ім'я файлу поточного елемента DirectoryIterator

-   [« DirectoryIterator::getExtension](directoryiterator.getextension.html)
    
-   [DirectoryIterator::getGroup »](directoryiterator.getgroup.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Повертає ім'я файлу поточного елемента DirectoryIterator
    

# DirectoryIterator::getFilename

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getFilename — Повертає ім'я файлу поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getFilename(): string
```

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.html)

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getFilename()****

Приклад виведе список вмісту директорії, що містить скрипт.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::getBasename()](directoryiterator.getbasename.html) - Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator
-   [DirectoryIterator::getPath()](directoryiterator.getpath.html) - Повертає шлях до поточного елементу DirectoryIterator без імені файлу
-   [DirectoryIterator::getPathname()](directoryiterator.getpathname.html) - Повертає шлях та ім'я файлу поточного елемента DirectoryIterator
-   [pathinfo()](function.pathinfo.html) - Повертає інформацію про шлях до файлу