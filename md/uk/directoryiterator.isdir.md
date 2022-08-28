Визначає, чи є поточний елемент DirectoryIterator директорією

-   [« DirectoryIterator::getType](directoryiterator.gettype.html)
    
-   [DirectoryIterator::isDot »](directoryiterator.isdot.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Визначає, чи є поточний елемент DirectoryIterator директорією
    

# DirectoryIterator::isDir

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isDir — Визначає, чи є поточний елемент DirectoryIterator директорією

### Опис

```methodsynopsis
public DirectoryIterator::isDir(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.html) директорією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**якщо елемент є директорією, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isDir()****

Приклад виведе список вкладених директорій у директорії, що містить скрипт.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isDir()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
.
..
apples
bananas
pears
```

### Дивіться також

-   [DirectoryIterator::getType()](directoryiterator.gettype.html) - Визначає тип поточного елемента DirectoryIterator
-   [DirectoryIterator::isDot()](directoryiterator.isdot.html) - Визначає, чи є поточний елемент DirectoryIterator '.' або '..'
-   [DirectoryIterator::isFile()](directoryiterator.isfile.html) - Визначає, чи є поточний елемент DirectoryIterator звичайним файлом
-   [DirectoryIterator::isLink()](directoryiterator.islink.html) - Визначає, чи є поточний елемент DirectoryIterator символічним посиланням