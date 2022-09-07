---
navigation:
  - directoryiterator.isreadable.md: '« DirectoryIterator::isReadable'
  - directoryiterator.key.md: 'DirectoryIterator::key »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::isWritable'
---
# DirectoryIterator::isWritable

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isWritable — Визначає, чи доступний поточний елемент DirectoryIterator для запису

### Опис

```methodsynopsis
public DirectoryIterator::isWritable(): bool
```

Визначає, чи поточний елемент доступний. [DirectoryIterator](class.directoryiterator.md) для запису.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо файл або директорія доступні для запису, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isWritable()****

Приклад показує список файлів і директорій, які можуть бути відкриті для запису, розташовані в директорії, що містить скрипт, що виконується.

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    if ($fileinfo->isWritable()) {
        echo $fileinfo->getFilename() . "\n";
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

-   [DirectoryIterator::getPerms()](directoryiterator.getperms.md) - Повертає набір прав для поточного елемента DirectoryIterator item
-   [DirectoryIterator::isExecutable()](directoryiterator.isexecutable.md) - Визначає, чи поточний елемент DirectoryIterator виконується
-   [DirectoryIterator::isReadable()](directoryiterator.isreadable.md) - Визначає, чи доступний поточний елемент DirectoryIterator для читання
