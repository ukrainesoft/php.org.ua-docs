Перевіряє, чи порожня колекція

-   [« Ds\\Set::intersect](ds-set.intersect.html)
    
-   [Ds\\Set::join »](ds-set.join.html)
    
-   [PHP Manual](index.html)
    
-   [Набор](class.ds-set.html)
    
-   Перевіряє, чи порожня колекція
    

# ДсSet::isEmpty

(PECL ds >= 1.0.0)

ДсSet::isEmpty — Перевіряє, чи колекція порожня.

### Опис

```methodsynopsis
public Ds\Set::isEmpty(): bool
```

Перевіряє, чи колекція порожня.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо колекція порожня, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **ДсSet::isEmpty()****

```php
<?php
$a = new \Ds\Set([1, 2, 3]);
$b = new \Ds\Set();

var_dump($a->isEmpty());
var_dump($b->isEmpty());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```