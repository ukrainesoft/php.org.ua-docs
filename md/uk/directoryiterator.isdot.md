---
navigation:
  - directoryiterator.isdir.md: '« DirectoryIterator::isDir'
  - directoryiterator.isexecutable.md: 'DirectoryIterator::isExecutable »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::isDot'
---
# DirectoryIterator::isDot

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isDot — Визначає, чи є поточний елемент DirectoryIterator '.' або '..'

### Опис

```methodsynopsis
public DirectoryIterator::isDot(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.md) `.` або `..`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо елемент є `.` або `..`, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isDot()****

Приклад виведе список усіх файлів у директорії, крім `.` і `..`

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if (!$fileinfo->isDot()) {
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
-   [DirectoryIterator::isFile()](directoryiterator.isfile.md) - Визначає, чи є поточний елемент DirectoryIterator звичайним файлом
-   [DirectoryIterator::isLink()](directoryiterator.islink.md) - Визначає, чи є поточний елемент DirectoryIterator символічним посиланням
