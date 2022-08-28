Видаляє всі значення

-   [« Пара](class.ds-pair.html)
    
-   [Ds\\Pair::\_\_construct »](ds-pair.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Пара](class.ds-pair.html)
    
-   Видаляє всі значення
    

# ДсPair::clear

(No version information available, might only be in Git)

ДсPair::clear — Видаляє всі значення

### Опис

```methodsynopsis
public Ds\Pair::clear(): void
```

Видаляє всі значення з пари.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсPair::clear()****

```php
<?php
$pair = new \Ds\Pair("a", 1);
print_r($pair);

$pair->clear();
print_r($pair);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Pair Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Pair Object
(
)
```