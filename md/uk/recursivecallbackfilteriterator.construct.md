---
navigation:
  - class.recursivecallbackfilteriterator.md: « RecursiveCallbackFilterIterator
  - recursivecallbackfilteriterator.getchildren.md: 'RecursiveCallbackFilterIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursivecallbackfilteriterator.md: RecursiveCallbackFilterIterator
title: 'RecursiveCallbackFilterIterator::construct'
---
# RecursiveCallbackFilterIterator::construct

(PHP 5> = 5.4.0, PHP 7, PHP 8)

RecursiveCallbackFilterIterator::construct — Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator

### Опис

public **RecursiveCallbackFilterIterator::construct**[RecursiveIterator](class.recursiveiterator.md) `$iterator` [callable](language.types.callable.md) `$callback`

Створює ітератор, що фільтрує, на основі об'єкта-ітератора. [RecursiveIterator](class.recursiveiterator.md), використовуючи функцію `callback` для відбору необхідних елементів.

### Список параметрів

`iterator`

Рекурсивний ітератор, якого потрібно застосувати фільтр.

`callback`

Callback-функція, яка має повертати **`true`**, якщо поточний елемент підходить під умови фільтра, та \*\*`false`\*\*якщо елемент потрібно виключити з перебору. Дивіться [Приклади](class.recursivecallbackfilteriterator.md#recursivecallbackfilteriterator.examples)

Може бути будь-яким допустимим [callable](language.types.callable.md) значенням.

### Дивіться також

-   [Приклади використання RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.md#recursivecallbackfilteriterator.examples)
-   [RecursiveCallbackFilterIterator::getChildren()](recursivecallbackfilteriterator.getchildren.md) - Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator
-   [RecursiveCallbackFilteriterator::hasChildren()](recursivecallbackfilteriterator.haschildren.md) - Перевіряє, чи містить поточний елемент внутрішнього ітератора дочірні елементи
