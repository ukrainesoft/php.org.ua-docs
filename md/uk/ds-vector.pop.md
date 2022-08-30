Видаляє та повертає останнє значення

-   [« DsVector::merge](ds-vector.merge.html)
    
-   [ДсVector::push »](ds-vector.push.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Видаляє та повертає останнє значення
    

# ДсVector::pop

(PECL ds >= 1.0.0)

ДсVector::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
public Ds\Vector::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::pop()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);

var_dump($vector->pop());
var_dump($vector->pop());
var_dump($vector->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(2)
int(1)
```