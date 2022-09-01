---
navigation:
  - directoryiterator.isfile.html: '« DirectoryIterator::isFile'
  - directoryiterator.isreadable.html: 'DirectoryIterator::isReadable »'
  - index.html: PHP Manual
  - class.directoryiterator.html: DirectoryIterator
title: 'DirectoryIterator::isLink'
---
# DirectoryIterator::isLink

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::isLink — Визначає, чи є поточний елемент DirectoryIterator символічним посиланням

### Опис

```methodsynopsis
public DirectoryIterator::isLink(): bool
```

Визначає, чи є поточний елемент [DirectoryIterator](class.directoryiterator.html) символічним посиланням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо елемент є символічним посиланням, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::isLink()****

Приклад містить рекурсивну функцію видалення дерева каталогів.

```php
<?php
/**
 * Данная функция рекурсивно удаляет все файлы, символические ссылки и директории
 * по указанному пути.
 *
 * @param string $path Путь к директории для удаления.
 */
function removeDir($path) {
    $dir = new DirectoryIterator($path);
    foreach ($dir as $fileinfo) {
        if ($fileinfo->isFile() || $fileinfo->isLink()) {
            unlink($fileinfo->getPathName());
        } elseif (!$fileinfo->isDot() && $fileinfo->isDir()) {
            removeDir($fileinfo->getPathName());
        }
    }
    rmdir($path);
}

removeDir('foo');
?>
```

### Дивіться також

-   [DirectoryIterator::getType()](directoryiterator.gettype.html) - Визначає тип поточного елемента DirectoryIterator
-   [DirectoryIterator::isDir()](directoryiterator.isdir.html) - Визначає, чи є поточний елемент DirectoryIterator директорією
-   [DirectoryIterator::isDot()](directoryiterator.isdot.html) - Визначає, чи є поточний елемент DirectoryIterator '.' або '..'
-   [DirectoryIterator::isFile()](directoryiterator.isfile.html) - Визначає, чи є поточний елемент DirectoryIterator звичайним файлом
