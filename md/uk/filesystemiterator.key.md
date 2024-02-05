---
navigation:
  - filesystemiterator.getflags.md: '« FilesystemIterator::getFlags'
  - filesystemiterator.next.md: 'FilesystemIterator::next »'
  - index.md: PHP Manual
  - class.filesystemiterator.md: FilesystemIterator
title: 'FilesystemIterator::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FilesystemIterator::key

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

FilesystemIterator::key — Визначення ключа поточного файлу

### Опис

```methodsynopsis
public FilesystemIterator::key(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях або ім'я файлу, залежно від встановлених прапорів. Дивіться [Константи FilesystemIterator](class.filesystemiterator.md#filesystemiterator.constants)

### Приклади

**Приклад #1 Приклад використання** FilesystemIterator::key()\*\*\*\*

Цей приклад виведе список вмісту директорії, в якій розташований скрипт.

```php
<?php
$iterator = new FilesystemIterator(dirname(__FILE__), FilesystemIterator::KEY_AS_FILENAME);
foreach ($iterator as $fileinfo) {
    echo $iterator->key() . "\n";
}
?>
```

Результат виконання наведеного прикладу PHP 8.2 аналогічний:

```
.
..
apple.jpg
banana.jpg
example.php
```

### Дивіться також

-   [FilesystemIterator constants](class.filesystemiterator.md#filesystemiterator.constants)
-   [DirectoryIterator::key()](directoryiterator.key.md) \- Повертає ключ для поточного елемента DirectoryIterator
-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) \- Повертає ім'я файлу поточного елемента DirectoryIterator
-   **DirectoryIterator::getPathname()**
