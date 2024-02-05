---
navigation:
  - callbackfilteriterator.accept.md: '« CallbackFilterIterator::accept'
  - class.directoryiterator.md: DirectoryIterator »
  - index.md: PHP Manual
  - class.callbackfilteriterator.md: CallbackFilterIterator
title: 'CallbackFilterIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# CallbackFilterIterator::\_\_construct

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

CallbackFilterIterator::\_\_construct — Створює ітератор, що фільтрує, на основі іншого ітератора.

### Опис

public**CallbackFilterIterator::\_\_construct** [Iterator](class.iterator.md) `$iterator` [callable](language.types.callable.md) `$callback`) .

Створює ітератор, що фільтрує, використовуючи функцію `callback` для відбору чи відхилення елементів.

### Список параметрів

`iterator`

Ітератор, до якого застосовується фільтр.

`callback`

Callback-функція, яка має повертати **`true`**, якщо поточний елемент пройшов фільтр, та **`false`**, якщо елемент відхилено. Дивіться [приклади](class.callbackfilteriterator.md#callbackfilteriterator.examples)

Можливо будь-яким [callable](language.types.callable.md)значением.

### Дивіться також

-   [Приклади використання CallbackFilterIterator](class.callbackfilteriterator.md#callbackfilteriterator.examples)
-   [CallbackFilterIterator::accept()](callbackfilteriterator.accept.md) \- Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик
