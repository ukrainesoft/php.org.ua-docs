Переміщує ітератор на задану позицію

-   [« LimitIterator::rewind](limititerator.rewind.html)
    
-   [LimitIterator::valid »](limititerator.valid.html)
    
-   [PHP Manual](index.html)
    
-   [LimitIterator](class.limititerator.html)
    
-   Переміщує ітератор на задану позицію
    

# LimitIterator::seek

(PHP 5> = 5.1.0, PHP 7, PHP 8)

LimitIterator::seek - Переміщує ітератор на задану позицію

### Опис

```methodsynopsis
public LimitIterator::seek(int $offset): int
```

Переміщує покажчик на задану позицію `offset`

### Список параметрів

`offset`

Позиція, яку потрібно перемістити покажчик.

### Значення, що повертаються

Повертає усунення від початкової позиції після переміщення.

### Помилки

Викидає виняток [OutOfBoundsException](class.outofboundsexception.html)якщо задана позиція виходить за межі, передані конструктору [LimitIterator::\_\_construct()](limititerator.construct.html)

### Дивіться також

-   [LimitIterator::current()](limititerator.current.html) - Отримання поточного елемента
-   [LimitIterator::key()](limititerator.key.html) - Отримання поточного ключа
-   [LimitIterator::rewind()](limititerator.rewind.html) - Переміщує покажчик на початкову позицію
-   [LimitIterator::next()](limititerator.next.html) - Переміщення до наступної позиції
-   [LimitIterator::valid()](limititerator.valid.html) - Перевіряє валідність поточного елемента