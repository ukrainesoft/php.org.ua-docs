---
navigation:
  - directoryiterator.getextension.md: '« DirectoryIterator::getExtension'
  - directoryiterator.isdot.md: 'DirectoryIterator::isDot »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::getFilename'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::getFilename

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getFilename — Повертає ім'я файлу поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getFilename(): string
```

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::getFilename()\*\*\*\*

У цьому прикладі буде виведено вміст каталогу, що містить скрипт.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo->getFilename() . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::getBasename()](directoryiterator.getbasename.md) \- Отримує базове ім'я поточного елемента DirectoryIterator
-   **DirectoryIterator::getPath()**
-   **DirectoryIterator::getPathname()**
-   [pathinfo()](function.pathinfo.md) \- Повертає інформацію про шлях до файлу
