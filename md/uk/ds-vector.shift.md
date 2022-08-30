Видаляє та повертає перше значення

-   [« DsVector::set](ds-vector.set.html)
    
-   [ДсVector::slice »](ds-vector.slice.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Видаляє та повертає перше значення
    

# ДсVector::shift

(PECL ds >= 1.0.0)

ДсVector::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
public Ds\Vector::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::shift()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->shift());
var_dump($vector->shift());
var_dump($vector->shift());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```