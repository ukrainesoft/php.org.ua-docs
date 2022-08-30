Перевіряє, чи порожній вектор

-   [« DsVector::insert](ds-vector.insert.html)
    
-   [ДсVector::join »](ds-vector.join.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Перевіряє, чи порожній вектор
    

# ДсVector::isEmpty

(PECL ds >= 1.0.0)

ДсVector::isEmpty — Перевіряє, чи порожній вектор

### Опис

```methodsynopsis
public Ds\Vector::isEmpty(): bool
```

Перевіряє, чи вектор порожній.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо вектор порожній, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсVector::isEmpty()****

```php
<?php
$a = new \Ds\Vector([1, 2, 3]);
$b = new \Ds\Vector();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```