---
navigation:
  - function.spl-autoload.md: « spl\_autoload
  - function.spl-object-hash.md: spl\_object\_hash »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_classes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_classes

(PHP 5, PHP 7, PHP 8)

spl\_classes — Повертає доступні класи SPL

### Опис

```methodsynopsis
spl_classes(): array
```

Ця функція повертає масив з доступними класами SPL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) з доступними нині класами SPL.

### Приклади

**Пример #1 Пример использования**spl\_classes()\*\*\*\*

```php
<?php

print_r(spl_classes());

?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [ArrayObject] => ArrayObject
    [ArrayIterator] => ArrayIterator
    [CachingIterator] => CachingIterator
    [RecursiveCachingIterator] => RecursiveCachingIterator
    [DirectoryIterator] => DirectoryIterator
    [FilterIterator] => FilterIterator
    [LimitIterator] => LimitIterator
    [ParentIterator] => ParentIterator
    [RecursiveDirectoryIterator] => RecursiveDirectoryIterator
    [RecursiveIterator] => RecursiveIterator
    [RecursiveIteratorIterator] => RecursiveIteratorIterator
    [SeekableIterator] => SeekableIterator
    [SimpleXMLIterator] => SimpleXMLIterator
)
```
