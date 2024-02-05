---
navigation:
  - filesystemiterator.next.md: '« FilesystemIterator::next'
  - filesystemiterator.setflags.md: 'FilesystemIterator::setFlags »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::rewind

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::rewind — Переміщення покажчика на початок

### Опис

```methodsynopsis
public FilesystemIterator::rewind(): void
```

Перекладає покажчик початку директорії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** FilesystemIterator::rewind()\*\*\*\*

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);

echo $iterator->key() . "\n";

$iterator->next();
echo $iterator->key() . "\n";

$iterator->rewind();
echo $iterator->key() . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
apple.jpg
banana.jpg
apple.jpg
```

### Дивіться також

-   [DirectoryIterator::rewind()](directoryiterator.rewind.md) \- Перемотування ітератора DirectoryIterator назад до початку
