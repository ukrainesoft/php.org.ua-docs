Додає значення до кінця масиву

-   [« ArrayObject](class.arrayobject.md)
    
-   [ArrayObject::asort »](arrayobject.asort.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayObject](class.arrayobject.md)
    
-   Додає значення до кінця масиву
    

# ArrayObject::append

(PHP 5, PHP 7, PHP 8)

ArrayObject::append — Додає значення до кінця масиву

### Опис

```methodsynopsis
public ArrayObject::append(mixed $value): void
```

Додає нове значення наприкінці масиву.

> **Зауваження**
> 
> Цей метод не може бути викликаний, якщо [ArrayObject](class.arrayobject.md) був створений із об'єкта. У цьому випадку використовуйте замість нього [ArrayObject::offsetSet()](arrayobject.offsetset.md)

### Список параметрів

`value`

Значення, яке потрібно додати.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::append()****

```php
<?php
$arrayobj = new ArrayObject(array('first','second','third'));
$arrayobj->append('fourth');
$arrayobj->append(array('five', 'six'));
var_dump($arrayobj);
?>
```

Результат виконання цього прикладу:

```
object(ArrayObject)#1 (5) {
  [0]=>
  string(5) "first"
  [1]=>
  string(6) "second"
  [2]=>
  string(5) "third"
  [3]=>
  string(6) "fourth"
  [4]=>
  array(2) {
    [0]=>
    string(4) "five"
    [1]=>
    string(3) "six"
  }
}
```

### Дивіться також

-   [ArrayObject::offsetSet()](arrayobject.offsetset.md) - Встановлює нове значення за вказаним індексом