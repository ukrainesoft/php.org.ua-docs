Встановлює нове значення за заданим індексом

-   [« SplFixedArray::offsetGet](splfixedarray.offsetget.md)
    
-   [SplFixedArray::offsetUnset »](splfixedarray.offsetunset.md)
    
-   [PHP Manual](index.md)
    
-   [SplFixedArray](class.splfixedarray.md)
    
-   Встановлює нове значення за заданим індексом
    

# SplFixedArray::offsetSet

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::offsetSet — Встановлює нове значення за заданим індексом

### Опис

```methodsynopsis
public SplFixedArray::offsetSet(int $index, mixed $value): void
```

За індексом `index` встановлює значення `value`

### Список параметрів

`index`

Індекс, яким встановлюється значення.

`value`

Нове значення для індексу `index`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [RuntimeException](class.runtimeexception.md), коли `index` перевищує заданий розмір масиву або коли `index` не можна розпізнати як ціле число.