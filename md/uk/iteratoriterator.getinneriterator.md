Отримує внутрішній ітератор

-   [« IteratorIterator::current](iteratoriterator.current.html)
    
-   [IteratorIterator::key »](iteratoriterator.key.html)
    
-   [PHP Manual](index.html)
    
-   [IteratorIterator](class.iteratoriterator.html)
    
-   Отримує внутрішній ітератор
    

# IteratorIterator::getInnerIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

IteratorIterator::getInnerIterator — Отримує внутрішній ітератор

### Опис

```methodsynopsis
public IteratorIterator::getInnerIterator(): ?Iterator
```

Отримує внутрішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Внутрішній ітератор, який було передано методу [IteratorIterator::\_\_construct()](iteratoriterator.construct.html) або **`null`**якщо внутрішній ітератор відсутній.

### Дивіться також

-   [Iterator](class.iterator.html)
-   [OuterIterator](class.outeriterator.html)