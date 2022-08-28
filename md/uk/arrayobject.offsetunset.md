Видаляє значення за вказаним індексом

-   [« ArrayObject::offsetSet](arrayobject.offsetset.html)
    
-   [ArrayObject::serialize »](arrayobject.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Видаляє значення за вказаним індексом
    

# ArrayObject::offsetUnset

(PHP 5, PHP 7, PHP 8)

ArrayObject::offsetUnset — Видаляє значення за вказаним індексом

### Опис

```methodsynopsis
public ArrayObject::offsetUnset(mixed $key): void
```

Видаляє значення за вказаним індексом.

### Список параметрів

`key`

Індекс, значення якого потрібно видалити.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::offsetUnset()****

```php
<?php
$arrayobj = new ArrayObject(array(0=>'zero',2=>'two'));
$arrayobj->offsetUnset(2);
var_dump($arrayobj);
?>
```

Результат виконання цього прикладу:

```
object(ArrayObject)#1 (1) {
  [0]=>
  string(4) "zero"
}
```