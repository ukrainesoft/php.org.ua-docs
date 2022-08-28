Повертає поточний елемент масиву

-   [« SplFixedArray::count](splfixedarray.count.html)
    
-   [SplFixedArray::fromArray »](splfixedarray.fromarray.html)
    
-   [PHP Manual](index.html)
    
-   [SplFixedArray](class.splfixedarray.html)
    
-   Повертає поточний елемент масиву
    

# SplFixedArray::current

(PHP 5> = 5.3.0, PHP 7)

SplFixedArray::current — Повертає поточний елемент масиву

### Опис

```methodsynopsis
public SplFixedArray::current(): mixed
```

Отримує поточний елемент масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний елемент масиву.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.html)коли внутрішній покажчик масиву вказує на неправильний індекс або вийшов за допустимі межі.