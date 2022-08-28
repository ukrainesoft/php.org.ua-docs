Створює копію ArrayObject

-   [« ArrayObject::exchangeArray](arrayobject.exchangearray.html)
    
-   [ArrayObject::getFlags »](arrayobject.getflags.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Створює копію ArrayObject
    

# ArrayObject::getArrayCopy

(PHP 5, PHP 7, PHP 8)

ArrayObject::getArrayCopy — Створює копію ArrayObject

### Опис

```methodsynopsis
public ArrayObject::getArrayCopy(): array
```

Експортує [ArrayObject](class.arrayobject.html) у масив.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає копію масиву. Якщо [ArrayObject](class.arrayobject.html) посилається на об'єкт, то буде повернено масив властивостей даного об'єкта.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getArrayCopy()****

```php
<?php
// Массив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);
$fruitsArrayObject['pears'] = 4;

// Создать копию массива
$copy = $fruitsArrayObject->getArrayCopy();
print_r($copy);

?>
```

Результат виконання цього прикладу:

```
Array
(
    [lemons] => 1
    [oranges] => 4
    [bananas] => 5
    [apples] => 10
    [pears] => 4
)
```