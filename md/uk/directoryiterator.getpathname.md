---
navigation:
  - directoryiterator.getpath.md: '« DirectoryIterator::getPath'
  - directoryiterator.getperms.md: 'DirectoryIterator::getPerms »'
  - index.md: PHP Manual
  - class.directoryiterator.md: DirectoryIterator
title: 'DirectoryIterator::getPathname'
---
# DirectoryIterator::getPathname

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getPathname — Повертає шлях та ім'я файлу поточного елемента DirectoryIterator

### Опис

```methodsynopsis
public DirectoryIterator::getPathname(): string
```

Повертає шлях та ім'я поточного файлу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях та ім'я поточного файлу. Директорія не міститиме завершального слішу.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getPathname()****

```php
<?php
$iterator = new DirectoryIterator(dirname(__FILE__));
foreach ($iterator as $fileinfo) {
    echo $fileinfo->getPathname() . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
/home/examples/.
/home/examples/..
/home/examples/apple.jpg
/home/examples/banana.jpg
/home/examples/getpathname.php
/home/examples/pear.jpg
```

### Дивіться також

-   [DirectoryIterator::getBasename()](directoryiterator.getbasename.md) - Повертає ім'я файлу (без розширення) поточного елемента DirectoryIterator
-   [DirectoryIterator::getFilename()](directoryiterator.getfilename.md) - Повертає ім'я файлу поточного елемента DirectoryIterator
-   [DirectoryIterator::getPath()](directoryiterator.getpath.md) - Повертає шлях до поточного елементу DirectoryIterator без імені файлу
-   [pathinfo()](function.pathinfo.md) - Повертає інформацію про шлях до файлу
