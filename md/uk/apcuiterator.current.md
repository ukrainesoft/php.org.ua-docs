---
navigation:
  - apcuiterator.construct.md: '« APCUIterator::construct'
  - apcuiterator.gettotalcount.md: 'APCUIterator::getTotalCount »'
  - index.md: PHP Manual
  - class.apcuiterator.md: APCUIterator
title: 'APCUIterator::current'
---
# APCUIterator::current

(PECL apcu >= 5.0.0)

APCUIterator::current — Отримати поточний елемент

### Опис

```methodsynopsis
public APCUIterator::current(): mixed
```

Отримує поточний елемент стека [APCUIterator](class.apcuiterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає поточний елемент або **`false`**, якщо елементів більше немає або виникла помилка.

### Дивіться також

-   [APCUIterator::next()](apcuiterator.next.md) - Переміщує покажчик на наступний елемент
-   [Iterator::current()](iterator.current.md) - Повернення поточного елемента
