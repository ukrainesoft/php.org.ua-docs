---
navigation:
  - limititerator.construct.md: '« LimitIterator::\_\_construct'
  - limititerator.getposition.md: 'LimitIterator::getPosition »'
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::current'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LimitIterator::current

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

LimitIterator::current — Отримання поточного елемента

### Опис

```methodsynopsis
public LimitIterator::current(): mixed
```

Отримує поточний елемент, на який посилається внутрішній покажчик [Iterator](class.iterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний елемент або \*\*`null`\*\*якщо такого немає.

### Дивіться також

-   [LimitIterator::key()](limititerator.key.md) \- Отримання поточного ключа
-   [LimitIterator::next()](limititerator.next.md) \- Переміщення до наступної позиції
-   [LimitIterator::rewind()](limititerator.rewind.md) \- Переміщує покажчик на початкову позицію
-   [LimitIterator::seek()](limititerator.seek.md) \- переміщує ітератор на задану позицію
-   [LimitIterator::valid()](limititerator.valid.md) \- Перевіряє валідність поточного елемента
