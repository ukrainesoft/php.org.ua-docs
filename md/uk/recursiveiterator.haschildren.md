---
navigation:
  - recursiveiterator.getchildren.md: '« RecursiveIterator::getChildren'
  - class.seekableiterator.md: SeekableIterator »
  - index.md: PHP Manual
  - class.recursiveiterator.md: RecursiveIterator
title: 'RecursiveIterator::hasChildren'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveIterator::hasChildren

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveIterator::hasChildren — Визначає, чи можна створити ітератор для поточного елемента.

### Опис

```methodsynopsis
public RecursiveIterator::hasChildren(): bool
```

Визначає, чи можна для поточного елемента створити ітератор методом [RecursiveIterator::getChildren()](recursiveiterator.getchildren.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо за поточним елементом можна здійснювати ітерацію, **`false`** в іншому випадку.

### Дивіться також

-   [RecursiveIterator::getChildren()](recursiveiterator.getchildren.md) \- Повертає ітератор для поточного елемента
