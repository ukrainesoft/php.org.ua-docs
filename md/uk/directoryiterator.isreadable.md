---
navigation:
  - directoryiterator.islink.md: '« DirectoryIterator::isLink'
  - directoryiterator.iswritable.md: 'DirectoryIterator::isWritable »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::isReadable'
---
# DirectoryIterator::isReadable

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isReadable — Визначає, чи доступний поточний елемент DirectoryIterator для читання

### Опис

```methodsynopsis
public DirectoryIterator::isReadable(): bool
```

Визначає, чи поточний елемент доступний. [DirectoryIterator](class.directoryiterator.md) для читання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл доступний для читання, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isReadable()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isReadable()) {
        echo $fileinfo->getFilename() . "\n";
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

-   [DirectoryIterator::isExecutable()](directoryiterator.isexecutable.md) - Визначає, чи поточний елемент DirectoryIterator виконується
-   [DirectoryIterator::isWritable()](directoryiterator.iswritable.md) - Визначає, чи доступний поточний елемент DirectoryIterator для запису
-   [DirectoryIterator::getPerms()](directoryiterator.getperms.md) - Повертає набір прав для поточного елемента DirectoryIterator item
