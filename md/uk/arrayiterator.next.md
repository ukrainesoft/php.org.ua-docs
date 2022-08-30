Переміщує покажчик за наступний запис

-   [« ArrayIterator::natsort](arrayiterator.natsort.md)
    
-   [ArrayIterator::offsetExists »](arrayiterator.offsetexists.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayIterator](class.arrayiterator.md)
    
-   Переміщує покажчик за наступний запис
    

# ArrayIterator::next

(PHP 5, PHP 7, PHP 8)

ArrayIterator::next — Переміщує покажчик за наступний запис

### Опис

```methodsynopsis
public ArrayIterator::next(): void
```

Переміщує покажчик на наступний запис у масиві.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::next()****

```php
<?php
$arrayobject = new ArrayObject();

$arrayobject[] = 'zero';
$arrayobject[] = 'one';

$iterator = $arrayobject->getIterator();

while($iterator->valid()) {
    echo $iterator->key() . ' => ' . $iterator->current() . "\n";

    $iterator->next();
}
?>
```

Результат виконання цього прикладу:

```
0 => zero
1 => one
```