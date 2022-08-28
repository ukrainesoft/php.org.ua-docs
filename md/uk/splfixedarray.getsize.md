Отримує розмір масиву

-   [« SplFixedArray::fromArray](splfixedarray.fromarray.html)
    
-   [SplFixedArray::key »](splfixedarray.key.html)
    
-   [PHP Manual](index.html)
    
-   [SplFixedArray](class.splfixedarray.html)
    
-   Отримує розмір масиву
    

# SplFixedArray::getSize

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplFixedArray::getSize — Отримує розмір масиву

### Опис

```methodsynopsis
public SplFixedArray::getSize(): int
```

Отримує розмір масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає розмір масиву як int.

### Приклади

**Приклад #1 Приклад використання **SplFixedArray::getSize()****

```php
<?php
$array = new SplFixedArray(5);
echo $array->getSize()."\n";
$array->setSize(10);
echo $array->getSize()."\n";
?>
```

Результат виконання цього прикладу:

```
5
10
```

### Примітки

> **Зауваження**
> 
> Даний метод еквівалентний [SplFixedArray::count()](splfixedarray.count.html)

### Дивіться також

-   [SplFixedArray::count()](splfixedarray.count.html) - Повертає розмір масиву