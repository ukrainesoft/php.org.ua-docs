---
navigation:
  - class.recursiveiterator.md: « RecursiveIterator
  - recursiveiterator.haschildren.md: 'RecursiveIterator::hasChildren »'
  - index.md: PHP Manual
  - class.recursiveiterator.md: RecursiveIterator
title: 'RecursiveIterator::getChildren'
---
# RecursiveIterator::getChildren

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveIterator::getChildren — Повертає ітератор до поточного елемента

### Опис

```methodsynopsis
public RecursiveIterator::getChildren(): ?RecursiveIterator
```

Повертає ітератор до поточного елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ітератор для поточного запису, якщо він існує або **`null`** в іншому випадку.

### Дивіться також

-   [RecursiveIterator::hasChildren()](recursiveiterator.haschildren.md) - Визначає, чи можна створити ітератор для поточного елемента.
