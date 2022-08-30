Повертає суму всіх значень колекції

-   [« DsSequence::sorted](ds-sequence.sorted.html)
    
-   [ДсSequence::unshift »](ds-sequence.unshift.html)
    
-   [PHP Manual](index.html)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Повертає суму всіх значень колекції
    

# ДсSequence::sum

(PECL ds >= 1.0.0)

ДсSequence::sum — Повертає суму всіх значень колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::sum(): int|float
```

Повертає суму всіх значень колекції.

> **Зауваження**
> 
> Масиви та об'єкти вважаються нулем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сума всіх значень колекції типу float або int, залежно від значень колекції.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::sum()** з цілими значеннями**

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->sum());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(6)
```

**Приклад #2 Приклад використання **ДсSequence::sum()** зі значеннями типу float**

```php
<?php
$sequence = new \Ds\Vector([1, 2.5, 3]);
var_dump($sequence->sum());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
float(6.5)
```