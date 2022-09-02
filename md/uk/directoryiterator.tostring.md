---
navigation:
  - directoryiterator.seek.md: '« DirectoryIterator::seek'
  - directoryiterator.valid.md: 'DirectoryIterator::valid »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::toString'
---
# DirectoryIterator::toString

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::toString — Повертає ім'я файлу у вигляді рядка

### Опис

```methodsynopsis
public
   DirectoryIterator::__toString(): string
```

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::toString()****

Приклад виведе список вмісту директорії, що містить скрипт.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo;
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
.
..
apple.jpg
banana.jpg
index.php
pear.jpg
```

### Дивіться також

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   Магічний метод [toString()](language.oop5.magic.md#object.tostring)
