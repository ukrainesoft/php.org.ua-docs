Визначає, чи поточний елемент DirectoryIterator виконується

-   [« DirectoryIterator::isDot](directoryiterator.isdot.html)
    
-   [DirectoryIterator::isFile »](directoryiterator.isfile.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Визначає, чи поточний елемент DirectoryIterator виконується
    

# DirectoryIterator::isExecutable

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isExecutable — Визначає, чи поточний елемент DirectoryIterator виконується

### Опис

```methodsynopsis
public DirectoryIterator::isExecutable(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.html) виконуваним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл є виконуваним, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isExecutable()****

Приклад показує список файлів, що виконуються в директорії, що містить виконуваний скрипт.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isExecutable()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
example.php
myscript.sh
```

### Дивіться також

-   [DirectoryIterator::isReadable()](directoryiterator.isreadable.html) - Визначає, чи доступний поточний елемент DirectoryIterator для читання
-   [DirectoryIterator::isWritable()](directoryiterator.iswritable.html) - Визначає, чи доступний поточний елемент DirectoryIterator для запису
-   [DirectoryIterator::getPerms()](directoryiterator.getperms.html) - Повертає набір прав для поточного елемента DirectoryIterator item