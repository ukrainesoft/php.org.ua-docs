---
navigation:
  - limititerator.rewind.md: '« LimitIterator::rewind'
  - limititerator.valid.md: 'LimitIterator::valid »'
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::seek'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LimitIterator::seek

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

LimitIterator::seek - Переміщує ітератор на задану позицію

### Опис

```methodsynopsis
public LimitIterator::seek(int $offset): int
```

Переміщує покажчик на задану позицію `offset`

### Список параметрів

`offset`

Позиція, яку потрібно перемістити покажчик.

### Значення, що повертаються

Повертає усунення від початкової позиції після переміщення.

### Помилки

Викидає виняток [OutOfBoundsException](class.outofboundsexception.md)якщо задана позиція виходить за межі, передані конструктору [LimitIterator::\_\_construct()](limititerator.construct.md)

### Дивіться також

-   [LimitIterator::current()](limititerator.current.md) \- Отримання поточного елемента
-   [LimitIterator::key()](limititerator.key.md) \- Отримання поточного ключа
-   [LimitIterator::rewind()](limititerator.rewind.md) \- Переміщує покажчик на початкову позицію
-   [LimitIterator::next()](limititerator.next.md) \- Переміщення до наступної позиції
-   [LimitIterator::valid()](limititerator.valid.md) \- Перевіряє валідність поточного елемента
