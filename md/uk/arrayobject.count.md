Отримати кількість загальнодоступних властивостей ArrayObject

-   [« ArrayObject::construct](arrayobject.construct.md)
    
-   [ArrayObject::exchangeArray »](arrayobject.exchangearray.md)
    
-   [PHP Manual](index.md)
    
-   [ArrayObject](class.arrayobject.md)
    
-   Отримати кількість загальнодоступних властивостей ArrayObject
    

# ArrayObject::count

(PHP 5, PHP 7, PHP 8)

ArrayObject::count — Отримати кількість загальнодоступних властивостей ArrayObject

### Опис

```methodsynopsis
public ArrayObject::count(): int
```

Отримати кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.md)

> **Зауваження**
> 
> Якщо [ArrayObject](class.arrayobject.md) створюється з масиву, всі властивості є загальнодоступними.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::count()****

```php
<?php
class Example {
    public $public = 'prop:public';
    private $prv   = 'prop:private';
    protected $prt = 'prop:protected';
}

$arrayobj = new ArrayObject(new Example());
var_dump($arrayobj->count());

$arrayobj = new ArrayObject(array('first','second','third'));
var_dump($arrayobj->count());
?>
```

Результат виконання цього прикладу:

```
int(1)
int(3)
```