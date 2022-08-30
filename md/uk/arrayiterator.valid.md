Перевіряє, чи містить масив ще запису

-   [« ArrayIterator::unserialize](arrayiterator.unserialize.html)
    
-   [CachingIterator »](class.cachingiterator.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayIterator](class.arrayiterator.html)
    
-   Перевіряє, чи містить масив ще запису
    

# ArrayIterator::valid

(PHP 5, PHP 7, PHP 8)

ArrayIterator::valid — Перевіряє, чи масив ще запису

### Опис

```methodsynopsis
public ArrayIterator::valid(): bool
```

Перевіряє, чи масив array містить ще записи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо ітератор дійсний і **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::valid()****

```php
<?php
$array = array('1' => 'one');

$arrayobject = new ArrayObject($array);
$iterator = $arrayobject->getIterator();

var_dump($iterator->valid()); //bool(true)

$iterator->next(); // перемещаем указатель на следующий элемент

//bool(false) потому что в массиве только один элемент
var_dump($iterator->valid());
?>
```