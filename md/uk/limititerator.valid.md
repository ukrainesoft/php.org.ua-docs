---
navigation:
  - limititerator.seek.md: '« LimitIterator::seek'
  - class.multipleiterator.md: MultipleIterator »
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::valid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LimitIterator::valid

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

LimitIterator::valid — Перевірка валідності поточного елемента

### Опис

```methodsynopsis
public LimitIterator::valid(): bool
```

Перевіряє, чи поточний елемент має допустиме значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [LimitIterator::current()](limititerator.current.md) \- Отримання поточного елемента
-   [LimitIterator::key()](limititerator.key.md) \- Отримання поточного ключа
-   [LimitIterator::rewind()](limititerator.rewind.md) \- Переміщує покажчик на початкову позицію
-   [LimitIterator::next()](limititerator.next.md) \- Переміщення до наступної позиції
-   [LimitIterator::seek()](limititerator.seek.md) \- переміщує ітератор на задану позицію
