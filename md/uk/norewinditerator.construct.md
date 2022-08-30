Створює новий об'єкт NoRewindIterator

-   [« NoRewindIterator](class.norewinditerator.md)
    
-   [NoRewindIterator::current »](norewinditerator.current.md)
    
-   [PHP Manual](index.md)
    
-   [NoRewindIterator](class.norewinditerator.md)
    
-   Створює новий об'єкт NoRewindIterator
    

# NoRewindIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

NoRewindIterator::construct — Створює новий об'єкт NoRewindIterator

### Опис

public **NoRewindIterator::construct**[Iterator](class.iterator.md) `$iterator`

Створює новий об'єкт NoRewindIterator.

### Список параметрів

`iterator`

Ітератор, що використовується.

### Приклади

**Приклад #1 Приклад використання **NoRewindIterator::construct()****

Другий цикл нічого не виведе, оскільки ітератор використовується лише один раз і не може бути повернутий на початок.

```php
<?php
$fruit = array('яблоко', 'банан', 'клюква');

$arr = new ArrayObject($fruit);
$it  = new NoRewindIterator($arr->getIterator());

echo "Фрукт А:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}

echo "Фрукт Б:\n";
foreach( $it as $item ) {
    echo $item . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Фрукт А:
яблоко
банан
клюква
Фрукт Б:
```

### Дивіться також

-   [NoRewindIterator::valid()](norewinditerator.valid.md) - перевіряє ітератор