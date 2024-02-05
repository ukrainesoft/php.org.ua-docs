---
navigation:
  - directoryiterator.seek.md: '« DirectoryIterator::seek'
  - directoryiterator.valid.md: 'DirectoryIterator::valid »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DirectoryIterator::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::\_\_toString — Отримує ім'я файлу у вигляді рядка

### Опис

```methodsynopsis
public DirectoryIterator::__toString(): string
```

Отримує ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я файлу поточного елемента [DirectoryIterator](class.directoryiterator.md)

### Приклади

**Приклад #1 Приклад використання** DirectoryIterator::\_\_toString()\*\*\*\*

У цьому прикладі буде виведено вміст каталогу, що містить скрипт.

```php
<?php
$dir = new DirectoryIterator(dirname(__FILE__));
foreach ($dir as $fileinfo) {
    echo $fileinfo;
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

-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) \- Повертає ім'я файлу поточного елемента DirectoryIterator
-   Магічний метод[\_\_toString()](language.oop5.magic.md#object.tostring)
