Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator

-   [« RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)
    
-   [RecursiveCallbackFilterIterator::getChildren »](recursivecallbackfilteriterator.getchildren.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)
    
-   Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator
    

# RecursiveCallbackFilterIterator::construct

(PHP 5> = 5.4.0, PHP 7, PHP 8)

RecursiveCallbackFilterIterator::construct — Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator

### Опис

public **RecursiveCallbackFilterIterator::construct**[RecursiveIterator](class.recursiveiterator.html) `$iterator` [callable](language.types.callable.html) `$callback`

Створює ітератор, що фільтрує, на основі об'єкта-ітератора. [RecursiveIterator](class.recursiveiterator.html), використовуючи функцію `callback` для відбору необхідних елементів.

### Список параметрів

`iterator`

Рекурсивний ітератор, якого потрібно застосувати фільтр.

`callback`

Callback-функція, яка має повертати **`true`**, якщо поточний елемент підходить під умови фільтра, та \*\*`false`\*\*якщо елемент потрібно виключити з перебору. Дивіться [Примеры](class.recursivecallbackfilteriterator.html#recursivecallbackfilteriterator.examples)

Може бути будь-яким допустимим [callable](language.types.callable.html) значенням.

### Дивіться також

-   [Примеры использования RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html#recursivecallbackfilteriterator.examples)
-   [RecursiveCallbackFilterIterator::getChildren()](recursivecallbackfilteriterator.getchildren.html) - Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator
-   [RecursiveCallbackFilteriterator::hasChildren()](recursivecallbackfilteriterator.haschildren.html) - Перевіряє, чи містить поточний елемент внутрішнього ітератора дочірні елементи