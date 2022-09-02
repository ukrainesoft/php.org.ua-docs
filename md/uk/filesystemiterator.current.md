---
navigation:
  - filesystemiterator.construct.md: '« FilesystemIterator::construct'
  - filesystemiterator.getflags.md: 'FilesystemIterator::getFlags »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::current'
---
# FilesystemIterator::current

(PHP 5> = 5.3.0, PHP 7, PHP 8)

FilesystemIterator::current — Поточний файл

### Опис

```methodsynopsis
public FilesystemIterator::current(): string|SplFileInfo|FilesystemIterator
```

Витягує інформацію про поточний файл.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я файлу, інформація про файл, або $this, залежно від встановлених прапорів. Дивіться [Константи FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants)

### Приклади

**Приклад #1 Приклад використання **FilesystemIterator::current()****

У цьому прикладі буде виведено список вмісту директорії в якій знаходиться скрипт, що виконується.

```php
<?php
$iterator = new FilesystemIterator(__DIR__, FilesystemIterator::CURRENT_AS_PATHNAME);
foreach ($iterator as $fileinfo) {
    echo $iterator->current() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/www/examples/apple.jpg
/www/examples/banana.jpg
/www/examples/example.php
```

### Дивіться також

-   [Константи FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants)
-   [DirectoryIterator::current()](directoryiterator.current.md) - Повертає поточний елемент DirectoryIterator
-   [DirectoryIterator::getFileName()](directoryiterator.getfilename.md) - Повертає ім'я файлу поточного елемента DirectoryIterator
