---
navigation:
  - appenditerator.current.md: '« AppendIterator::current'
  - appenditerator.getinneriterator.md: 'AppendIterator::getInnerIterator »'
  - index.md: PHP Manual
  - class.appenditerator.md: AppendIterator
title: 'AppendIterator::getArrayIterator'
---
# AppendIterator::getArrayIterator

(PHP 5> = 5.2.0, PHP 7, PHP 8)

AppendIterator::getArrayIterator — Повертає клас ітератора масиву ArrayIterator

### Опис

```methodsynopsis
public AppendIterator::getArrayIterator(): ArrayIterator
```

Цей метод отримує клас [ArrayIterator](class.arrayiterator.md), який використовується для зберігання ітераторів, доданих за допомогою методу [AppendIterator::append()](appenditerator.append.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає клас [ArrayIterator](class.arrayiterator.md)містить додані ітератори.

### Дивіться також

-   [AppendIterator::getInnerIterator()](appenditerator.getinneriterator.md) - Повертає внутрішній ітератор
