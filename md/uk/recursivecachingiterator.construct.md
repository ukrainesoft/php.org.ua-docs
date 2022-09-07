---
navigation:
  - class.recursivecachingiterator.md: « RecursiveCachingIterator
  - recursivecachingiterator.getchildren.md: 'RecursiveCachingIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursivecachingiterator.md: RecursiveCachingIterator
title: 'RecursiveCachingIterator::construct'
---
# RecursiveCachingIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveCachingIterator::construct — Конструктор

### Опис

public **RecursiveCachingIterator::construct**[Iterator](class.iterator.md) `$iterator`, int `$flags` = RecursiveCachingIterator::CALLTOSTRING)

Створює новий [RecursiveCachingIterator](class.recursivecachingiterator.md), що складається з переданого ітератора (`iterator`

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`iterator`

Ітератор, що використовується.

`flags`

Прапори. Використовуйте **`CALL_TOSTRING`** для того, щоб викликати **RecursiveCachingIterator::toString()** для кожного елемента (за замовчуванням) та/або **`CATCH_GET_CHILD`** для перехоплення винятків під час спроби отримання дочірніх елементів.

### Дивіться також

-   [CachingIterator::construct()](cachingiterator.construct.md) - Створює новий об'єкт CachingIterator для ітератора
