Повертає, чи існує зазначений індекс

-   [« ArrayObject::natsort](arrayobject.natsort.html)
    
-   [ArrayObject::offsetGet »](arrayobject.offsetget.html)
    
-   [PHP Manual](index.html)
    
-   [ArrayObject](class.arrayobject.html)
    
-   Повертає, чи існує зазначений індекс
    

# ArrayObject::offsetExists

(PHP 5, PHP 7, PHP 8)

ArrayObject::offsetExists — Повертає, чи існує зазначений індекс

### Опис

```methodsynopsis
public ArrayObject::offsetExists(mixed $key): bool
```

### Список параметрів

`key`

Індекс, який має бути перевірений.

### Значення, що повертаються

\*\*`true`\*\*якщо зазначений індекс існує, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання **ArrayObject::offsetExists()****

```php
<?php
$arrayobj = new ArrayObject(array('zero', 'one', 'example'=>'e.g.'));
var_dump($arrayobj->offsetExists(1));
var_dump($arrayobj->offsetExists('example'));
var_dump($arrayobj->offsetExists('notfound'));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(true)
bool(false)
```