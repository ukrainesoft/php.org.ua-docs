---
navigation:
  - recursivetreeiterator.callhaschildren.md: '« RecursiveTreeIterator::callHasChildren'
  - recursivetreeiterator.current.md: 'RecursiveTreeIterator::current »'
  - index.md: PHP Manual
  - class.recursivetreeiterator.md: RecursiveTreeIterator
title: 'RecursiveTreeIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveTreeIterator::\_\_construct

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

RecursiveTreeIterator::\_\_construct — Конструктор класу RecursiveTreeIterator

### Опис

public **RecursiveTreeIterator::\_\_construct**  
[RecursiveIterator](class.recursiveiterator.md) [IteratorAggregate](class.iteratoraggregate.md) `$iterator`,  
int`$flags`\= RecursiveTreeIterator::BYPASS\_KEY,  
int`$cachingIteratorFlags`\= CachingIterator::CATCH\_GET\_CHILD,  
int`$mode`\= RecursiveTreeIterator::SELF\_FIRST  
) .

Створює новий об'єкт класу [RecursiveTreeIterator](class.recursivetreeiterator.md) на основі рекурсивного об'єкта-ітератора.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`iterator`

Об'єкт класу [RecursiveIterator](class.recursiveiterator.md)или класса[IteratorAggregate](class.iteratoraggregate.md)

`flags`

Прапори впливають поведінка деяких методів класу. Список можливих прапорів можна знайти на сторінці [Обумовлених констант RecursiveTreeIterator](class.recursivetreeiterator.md#recursivetreeiterator.constants)

`caching_it_flags`

Прапори для налаштування внутрішнього об'єкта [RecursiveCachingIterator](class.recursivecachingiterator.md)

`mode`

Прапори для налаштування внутрішнього об'єкта [RecursiveIteratorIterator](class.recursiveiteratoriterator.md)
