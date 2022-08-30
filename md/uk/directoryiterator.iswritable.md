Визначає, чи доступний поточний елемент DirectoryIterator для запису

-   [« DirectoryIterator::isReadable](directoryiterator.isreadable.html)
    
-   [DirectoryIterator::key »](directoryiterator.key.html)
    
-   [PHP Manual](index.html)
    
-   [DirectoryIterator](class.directoryiterator.html)
    
-   Визначає, чи доступний поточний елемент DirectoryIterator для запису
    

# DirectoryIterator::isWritable

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isWritable — Визначає, чи доступний поточний елемент DirectoryIterator для запису

### Опис

```methodsynopsis
public DirectoryIterator::isWritable(): bool
```

Визначає, чи поточний елемент доступний. [DirectoryIterator](class.directoryiterator.html) для запису.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл або директорія доступні для запису, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isWritable()****

Приклад показує список файлів і директорій, які можуть бути відкриті для запису, розташовані в директорії, що містить скрипт, що виконується.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isWritable()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apples.txt
bananas.html
pears
```

### Дивіться також

-   [DirectoryIterator::getPerms()](directoryiterator.getperms.html) - Повертає набір прав для поточного елемента DirectoryIterator item
-   [DirectoryIterator::isExecutable()](directoryiterator.isexecutable.html) - Визначає, чи поточний елемент DirectoryIterator виконується
-   [DirectoryIterator::isReadable()](directoryiterator.isreadable.html) - Визначає, чи доступний поточний елемент DirectoryIterator для читання