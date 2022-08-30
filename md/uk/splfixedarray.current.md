Повертає поточний елемент масиву

-   [« SplFixedArray::count](splfixedarray.count.md)
    
-   [SplFixedArray::fromArray »](splfixedarray.fromarray.md)
    
-   [PHP Manual](index.md)
    
-   [SplFixedArray](class.splfixedarray.md)
    
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

Викидає виняток [RuntimeException](class.runtimeexception.md)коли внутрішній покажчик масиву вказує на неправильний індекс або вийшов за допустимі межі.