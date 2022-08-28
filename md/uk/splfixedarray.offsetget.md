Повертає значення за вказаним індексом

-   [« SplFixedArray::offsetExists](splfixedarray.offsetexists.html)
    
-   [SplFixedArray::offsetSet »](splfixedarray.offsetset.html)
    
-   [PHP Manual](index.html)
    
-   [SplFixedArray](class.splfixedarray.html)
    
-   Повертає значення за вказаним індексом
    

# SplFixedArray::offsetGet

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::offsetGet — Повертає значення за вказаним індексом

### Опис

```methodsynopsis
public SplFixedArray::offsetGet(int $index): mixed
```

Повертає значення за індексом `index`

### Список параметрів

`index`

Індекс.

### Значення, що повертаються

Значення за індексом `index`

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.html), коли параметр `index` виходить за рамки заданого розміру масиву або коли `index` не можна розпізнати як ціле число.