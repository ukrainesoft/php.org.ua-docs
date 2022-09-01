---
navigation:
  - class.recursiveiterator.html: « RecursiveIterator
  - recursiveiterator.haschildren.html: 'RecursiveIterator::hasChildren »'
  - index.html: PHP Manual
  - class.recursiveiterator.html: RecursiveIterator
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

-   [RecursiveIterator::hasChildren()](recursiveiterator.haschildren.html) - Визначає, чи можна створити ітератор для поточного елемента.
