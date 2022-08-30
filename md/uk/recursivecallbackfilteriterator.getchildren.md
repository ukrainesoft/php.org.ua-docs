Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator

-   [« RecursiveCallbackFilterIterator::construct](recursivecallbackfilteriterator.construct.html)
    
-   [RecursiveCallbackFilterIterator::hasChildren »](recursivecallbackfilteriterator.haschildren.html)
    
-   [PHP Manual](index.html)
    
-   [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)
    
-   Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator
    

# RecursiveCallbackFilterIterator::getChildren

(PHP 5> = 5.4.0, PHP 7, PHP 8)

RecursiveCallbackFilterIterator::getChildren — Повертає дочірні елементи ітератора, що зберігається всередині RecursiveCallbackFilterIterator

### Опис

```methodsynopsis
public RecursiveCallbackFilterIterator::getChildren(): RecursiveCallbackFilterIterator
```

Вибирає дочірні елементи внутрішнього ітератора, які підходять під фільтрові умови.

Перш ніж викликати метод, необхідно впевнитись, що внутрішній ітератор містить дочірні елементи. Зробити це можна за допомогою методу [RecursiveCallbackFilterIterator::hasChildren()](recursivecallbackfilteriterator.haschildren.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html)містить дочірні елементи внутрішнього ітератора.

### Дивіться також

-   [Приклади використання RecursiveCallbackFilterIterator](class.recursivecallbackfilteriterator.html#recursivecallbackfilteriterator.examples)
-   [RecursiveCallbackFilterIterator::construct()](recursivecallbackfilteriterator.construct.html) - Створює об'єкт класу RecursiveCallbackFilterIterator на основі об'єкта RecursiveIterator
-   [RecursiveCallbackFilteriterator::hasChildren()](recursivecallbackfilteriterator.haschildren.html) - Перевіряє, чи містить поточний елемент внутрішнього ітератора дочірні елементи