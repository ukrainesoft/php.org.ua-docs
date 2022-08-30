Додає значення до кінця послідовності

-   [« DsSequence::pop](ds-sequence.pop.html)
    
-   [ДсSequence::reduce »](ds-sequence.reduce.html)
    
-   [PHP Manual](index.md)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Додає значення до кінця послідовності
    

# ДсSequence::push

(PECL ds >= 1.0.0)

ДсSequence::push — Додає значення до кінця послідовності

### Опис

```methodsynopsis
abstract public Ds\Sequence::push(mixed ...$values): void
```

Додає значення до кінця послідовності.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::push()****

```php
<?php
$sequence = new \Ds\Vector();

$sequence->push("a");
$sequence->push("b");
$sequence->push("c", "d");
$sequence->push(...["e", "f"]);

print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```