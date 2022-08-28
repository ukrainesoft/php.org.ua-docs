Створити новий ітератор із екземпляра ArrayObject

-   [« ArrayObject::getFlags](arrayobject.getflags.html)
    
-   [ArrayObject::getIteratorClass »](arrayobject.getiteratorclass.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Створити новий ітератор із екземпляра ArrayObject
    

# ArrayObject::getIterator

(PHP 5, PHP 7, PHP 8)

ArrayObject::getIterator — Створити новий ітератор із екземпляра ArrayObject

### Опис

```methodsynopsis
public ArrayObject::getIterator(): Iterator
```

Створити новий ітератор із екземпляра [ArrayObject](class.arrayobject.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ітератор із [ArrayObject](class.arrayobject.html)

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getIterator()****

```php
<?php
$array = array('1' => 'one',
               '2' => 'two',
               '3' => 'three');

$arrayobject = new ArrayObject($array);

$iterator = $arrayobject->getIterator();

while($iterator->valid()) {
    echo $iterator->key() . ' => ' . $iterator->current() . "\n";

    $iterator->next();
}
?>
```

Результат виконання цього прикладу:

```
1 => one
2 => two
3 => three
```