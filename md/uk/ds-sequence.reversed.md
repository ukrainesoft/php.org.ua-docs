Повертає перегорнуту копію колекції

-   [« DsSequence::reverse](ds-sequence.reverse.html)
    
-   [ДсSequence::rotate »](ds-sequence.rotate.html)
    
-   [PHP Manual](index.md)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Повертає перегорнуту копію колекції
    

# ДсSequence::reversed

(PECL ds >= 1.0.0)

ДсSequence::reversed — Повертає перегорнуту копію колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::reversed(): Ds\Sequence
```

Повертає копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перегорнута копія колекції.

> **Зауваження**
> 
> Поточна колекція не зміниться.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::reversed()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

print_r($sequence->reversed());
print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => c
    [1] => b
    [2] => a
)
Ds\Vector Object
(
    [0] => a
    [1] => b
    [2] => c
)
```