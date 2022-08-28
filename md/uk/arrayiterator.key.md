Повертає ключ поточного елемента масиву

-   [« ArrayIterator::getFlags](arrayiterator.getflags.html)
    
-   [ArrayIterator::ksort »](arrayiterator.ksort.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayIterator](class.arrayiterator.html)
    
-   Повертає ключ поточного елемента масиву
    

# ArrayIterator::key

(PHP 5, PHP 7, PHP 8)

ArrayIterator::key — Повертає ключ поточного елемента масиву

### Опис

```methodsynopsis
public ArrayIterator::key(): string|int|null
```

Ця функція повертає ключ поточного елемента масиву

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ поточного елемента у масиві (array).

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::key()****

```php
<?php
$array = array('key' => 'value');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

echo $iterator->key(); //key
?>
```