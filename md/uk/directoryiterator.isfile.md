---
navigation:
  - directoryiterator.isexecutable.md: '« DirectoryIterator::isExecutable'
  - directoryiterator.islink.md: 'DirectoryIterator::isLink »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::isFile'
---
# DirectoryIterator::isFile

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isFile — Визначає, чи поточний елемент DirectoryIterator є звичайним файлом.

### Опис

```methodsynopsis
public DirectoryIterator::isFile(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.md) звичайним файлом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл існує і є звичайним файлом (тобто не є `ссылкой` або `директорией`), інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isFile()****

Приклад виведе список всіх файлів у директорії, що містить скрипт, що виконується.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isFile()) {
        echo $fileinfo->getFilename() . "\n";
    }
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
apple.jpg
banana.jpg
example.php
pears.jpg
```

### Дивіться також

-   [DirectoryIterator::getType()](directoryiterator.gettype.md) - Визначає тип поточного елемента DirectoryIterator
-   [DirectoryIterator::isDir()](directoryiterator.isdir.md) - Визначає, чи є поточний елемент DirectoryIterator директорією
-   [DirectoryIterator::isDot()](directoryiterator.isdot.md) - Визначає, чи є поточний елемент DirectoryIterator '.' або '..'
-   [DirectoryIterator::isLink()](directoryiterator.islink.md) - Визначає, чи є поточний елемент DirectoryIterator символічним посиланням
