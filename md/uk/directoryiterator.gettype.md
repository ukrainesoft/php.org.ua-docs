---
navigation:
  - directoryiterator.getsize.md: '« DirectoryIterator::getSize'
  - directoryiterator.isdir.md: 'DirectoryIterator::isDir »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::getType'
---
# DirectoryIterator::getType

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getType — Визначає тип поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getType(): string
```

Визначає до якого типу належить поточний елемент [DirectoryIterator](class.directoryiterator.md). Можливі варіанти: `file` (файл), `link` (Посилання), або `dir` (Директорія).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string), який містить тип файлу. Можливі варіанти: `file` (файл), `link` (Посилання), або `dir` (Директорія).

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getType()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    echo $fileinfo->getFilename() . " " . $fileinfo->getType() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
. dir
.. dir
apple.jpg file
banana.jpg file
example.php file
pear.jpg file
```

### Дивіться також

-   [DirectoryIterator::isDir()](directoryiterator.isdir.md) - Визначає, чи є поточний елемент DirectoryIterator директорією
-   [DirectoryIterator::isDot()](directoryiterator.isdot.md) - Визначає, чи є поточний елемент DirectoryIterator '.' або '..'
-   [DirectoryIterator::isFile()](directoryiterator.isfile.md) - Визначає, чи є поточний елемент DirectoryIterator звичайним файлом
-   [DirectoryIterator::isLink()](directoryiterator.islink.md) - Визначає, чи є поточний елемент DirectoryIterator символічним посиланням
