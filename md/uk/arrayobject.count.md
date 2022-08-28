Отримати кількість загальнодоступних властивостей ArrayObject

-   [« ArrayObject::\_\_construct](arrayobject.construct.html)
    
-   [ArrayObject::exchangeArray »](arrayobject.exchangearray.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Отримати кількість загальнодоступних властивостей ArrayObject
    

# ArrayObject::count

(PHP 5, PHP 7, PHP 8)

ArrayObject::count — Отримати кількість загальнодоступних властивостей ArrayObject

### Опис

```methodsynopsis
public ArrayObject::count(): int
```

Отримати кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.html)

> **Зауваження**
> 
> Якщо [ArrayObject](class.arrayobject.html) створюється з масиву, всі властивості є загальнодоступними.

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