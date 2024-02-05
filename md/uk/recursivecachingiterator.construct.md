---
navigation:
  - class.recursivecachingiterator.md: « RecursiveCachingIterator
  - recursivecachingiterator.getchildren.md: 'RecursiveCachingIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursivecachingiterator.md: RecursiveCachingIterator
title: 'RecursiveCachingIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveCachingIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveCachingIterator::\_\_construct — Конструктор

### Опис

public **RecursiveCachingIterator::\_\_construct** [Iterator](class.iterator.md) `$iterator`, int`$flags`\= RecursiveCachingIterator::CALL\_TOSTRING)

Створює новий [RecursiveCachingIterator](class.recursivecachingiterator.md), що складається з переданого ітератора (`iterator`

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`iterator`

Ітератор, що використовується.

`flags`

Флаги. Используйте\*\*`CALL_TOSTRING`\*\* для того, щоб викликати **RecursiveCachingIterator::\_\_toString()** для кожного елемента (за замовчуванням) та/або **`CATCH_GET_CHILD`** для перехоплення винятків під час спроби отримання дочірніх елементів.

### Дивіться також

-   [CachingIterator::\_\_construct()](cachingiterator.construct.md) \- Створює новий об'єкт CachingIterator для ітератора
