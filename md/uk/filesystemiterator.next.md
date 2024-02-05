---
navigation:
  - filesystemiterator.key.md: '« FilesystemIterator::key'
  - filesystemiterator.rewind.md: 'FilesystemIterator::rewind »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::next

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::next — Переміщення вказівника на наступний файл

### Опис

```methodsynopsis
public FilesystemIterator::next(): void
```

Перехід до наступного файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**FilesystemIterator::next()\*\*\*\*

Виведення списку вмісту директорії за допомогою циклу while.

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__));
while($iterator->valid()) {
    echo $iterator->getFilename() . "\n";
    $iterator->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
apple.jpg
banana.jpg
example.php
```

### Дивіться також

-   [DirectoryIterator::next()](directoryiterator.next.md) \- Перехід до наступного елементу DirectoryIterator
