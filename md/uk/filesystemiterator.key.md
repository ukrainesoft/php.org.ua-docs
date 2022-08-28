Визначення ключа поточного файлу

-   [« FilesystemIterator::getFlags](filesystemiterator.getflags.html)
    
-   [FilesystemIterator::next »](filesystemiterator.next.html)
    
-   [PHP Manual](index.html)
    
-   [FilesystemIterator](class.filesystemiterator.html)
    
-   Визначення ключа поточного файлу
    

# FilesystemIterator::key

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::key — Визначення ключа поточного файлу

### Опис

```methodsynopsis
public FilesystemIterator::key(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях або ім'я файлу, залежно від встановлених прапорів. Дивіться [Константы FilesystemIterator](class.filesystemiterator.html#filesystemiterator.constants)

### Приклади

**Приклад #1 Приклад використання **FilesystemIterator::key()****

Цей приклад виведе список вмісту директорії, в якій розташований скрипт.

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);
foreach ($iterator as $fileinfo) {
    echo $iterator->key() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator constants](class.filesystemiterator.html#filesystemiterator.constants)
-   [DirectoryIterator::key()](directoryiterator.key.html) - Повертає ключ поточного елемента DirectoryIterator
-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.html) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getPathname()](directoryiterator.getpathname.html) - Повертає шлях та ім'я файлу поточного елемента DirectoryIterator