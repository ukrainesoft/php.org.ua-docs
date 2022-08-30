Створює копію ArrayObject

-   [« ArrayObject::exchangeArray](arrayobject.exchangearray.md)
    
-   [ArrayObject::getFlags »](arrayobject.getflags.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayObject](class.arrayobject.md)
    
-   Створює копію ArrayObject
    

# ArrayObject::getArrayCopy

(PHP 5, PHP 7, PHP 8)

ArrayObject::getArrayCopy — Створює копію ArrayObject

### Опис

```methodsynopsis
public ArrayObject::getArrayCopy(): array
```

Експортує [ArrayObject](class.arrayobject.md) у масив.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає копію масиву. Якщо [ArrayObject](class.arrayobject.md) посилається на об'єкт, то буде повернено масив властивостей даного об'єкта.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getArrayCopy()****

```php
<?php
// Масив с количеством фруктов
$fruits = array("lemons" => 1, "oranges" => 4, "bananas" => 5, "apples" => 10);

$fruitsArrayObject = new ArrayObject($fruits);
$fruitsArrayObject['pears'] = 4;

// Создать копию Масива
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