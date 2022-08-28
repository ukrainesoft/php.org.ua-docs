Конструктор

-   [« RecursiveCachingIterator](class.recursivecachingiterator.html)
    
-   [RecursiveCachingIterator::getChildren »](recursivecachingiterator.getchildren.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveCachingIterator](class.recursivecachingiterator.html)
    
-   Конструктор
    

# RecursiveCachingIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveCachingIterator::construct — Конструктор

### Опис

public **RecursiveCachingIterator::construct**[Iterator](class.iterator.html) `$iterator`, int `$flags` = RecursiveCachingIterator::CALLTOSTRING)

Створює новий [RecursiveCachingIterator](class.recursivecachingiterator.html), що складається з переданого ітератора (`iterator`

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`iterator`

Ітератор, що використовується.

`flags`

Прапори. Використовуйте **`CALL_TOSTRING`** для того, щоб викликати **RecursiveCachingIterator::toString()** для кожного елемента (за замовчуванням) та/або **`CATCH_GET_CHILD`** для перехоплення винятків під час спроби отримання дочірніх елементів.

### Дивіться також

-   [CachingIterator::\_\_construct()](cachingiterator.construct.html) - Створює новий об'єкт CachingIterator для ітератора