---
navigation:
  - function.spl-autoload.html: « splautoload
  - function.spl-object-hash.html: splobjecthash »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: splclasses
---
# splclasses

(PHP 5, PHP 7, PHP 8)

splclasses — Повертає доступні класи SPL

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

**Приклад #1 Приклад використання **splclasses()****

```php
<?php

print_r(spl_classes());

?>
```

Результатом виконання цього прикладу буде щось подібне:

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
