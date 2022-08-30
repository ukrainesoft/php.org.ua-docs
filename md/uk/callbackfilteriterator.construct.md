Створює ітератор, що фільтрує, на основі іншого ітератора.

-   [« CallbackFilterIterator::accept](callbackfilteriterator.accept.md)
    
-   [DirectoryIterator »](class.directoryiterator.md)
    
-   [PHP Manual](index.md)
    
-   [CallbackFilterIterator](class.callbackfilteriterator.md)
    
-   Створює ітератор, що фільтрує, на основі іншого ітератора.
    

# CallbackFilterIterator::construct

(PHP 5> = 5.4.0, PHP 7, PHP 8)

CallbackFilterIterator::construct — Створює ітератор, що фільтрує, на основі іншого ітератора.

### Опис

public **CallbackFilterIterator::construct**[Iterator](class.iterator.md) `$iterator` [callable](language.types.callable.md) `$callback`

Створює ітератор, що фільтрує, використовуючи функцію `callback` для відбору чи відхилення елементів.

### Список параметрів

`iterator`

Ітератор, до якого застосовується фільтр.

`callback`

Callback-функція, яка має повертати **`true`**, якщо поточний елемент пройшов фільтр, та **`false`**, якщо елемент відхилено. Дивіться [приклади](class.callbackfilteriterator.html#callbackfilteriterator.examples)

Можливо будь-яким [callable](language.types.callable.md) значенням.

### Дивіться також

-   [Приклади використання CallbackFilterIterator](class.callbackfilteriterator.html#callbackfilteriterator.examples)
-   [CallbackFilterIterator::accept()](callbackfilteriterator.accept.md) - Викликає callback-функцію та передає їй як аргументи поточне значення, поточний ключ та внутрішній покажчик