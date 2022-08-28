Конструктор класу RecursiveTreeIterator

-   [« RecursiveTreeIterator::callHasChildren](recursivetreeiterator.callhaschildren.html)
    
-   [RecursiveTreeIterator::current »](recursivetreeiterator.current.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveTreeIterator](class.recursivetreeiterator.html)
    
-   Конструктор класу RecursiveTreeIterator
    

# RecursiveTreeIterator::construct

(PHP 5> = 5.3.0, PHP 7, PHP 8)

RecursiveTreeIterator::construct — Конструктор класу RecursiveTreeIterator

### Опис

public **RecursiveTreeIterator::construct**  
[RecursiveIterator](class.recursiveiterator.html)[IteratorAggregate](class.iteratoraggregate.html) `$iterator`  
int `$flags` = RecursiveTreeIterator::BYPASSKEY,  
int `$cachingIteratorFlags` = CachingIterator::CATCHGETCHILD,  
int `$mode` = RecursiveTreeIterator::SELFFIRST  

Створює новий об'єкт класу [RecursiveTreeIterator](class.recursivetreeiterator.html) на основі рекурсивного об'єкта-ітератора.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`iterator`

Об'єкт класу [RecursiveIterator](class.recursiveiterator.html) або класу [IteratorAggregate](class.iteratoraggregate.html)

`flags`

Прапори впливають поведінка деяких методів класу. Список можливих прапорів можна знайти на сторінці [Предопределённых констант RecursiveTreeIterator](class.recursivetreeiterator.html#recursivetreeiterator.constants)

`caching_it_flags`

Прапори для налаштування внутрішнього об'єкта [RecursiveCachingIterator](class.recursivecachingiterator.html)

`mode`

Прапори для налаштування внутрішнього об'єкта [RecursiveIteratorIterator](class.recursiveiteratoriterator.html)