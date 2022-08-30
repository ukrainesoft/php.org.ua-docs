Видаляє та повертає значення за індексом

-   [« DsVector::reduce](ds-vector.reduce.html)
    
-   [ДсVector::reverse »](ds-vector.reverse.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Видаляє та повертає значення за індексом
    

# ДсVector::remove

(PECL ds >= 1.0.0)

ДсVector::remove — Видаляє та повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Vector::remove(int $index): mixed
```

Видаляє та повертає значення за індексом.

### Список параметрів

`index`

Індекс, яким необхідно видалити значення.

### Значення, що повертаються

Віддалене значення.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсVector::remove()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->remove(1));
var_dump($vector->remove(0));
var_dump($vector->remove(0));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "b"
string(1) "a"
string(1) "c"
```