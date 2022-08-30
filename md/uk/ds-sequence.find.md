Пошук індексу за значенням

-   [« DsSequence::filter](ds-sequence.filter.html)
    
-   [ДсSequence::first »](ds-sequence.first.html)
    
-   [PHP Manual](index.md)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Пошук індексу за значенням
    

# ДсSequence::find

(PECL ds >= 1.0.0)

ДсSequence::find — Пошук індексу за значенням

### Опис

```methodsynopsis
abstract public Ds\Sequence::find(mixed $value): mixed
```

Повертає індекс значення `value`, або \*\*`false`\*\*якщо нічого не знайдено.

### Список параметрів

`value`

Шукане значення.

### Значення, що повертаються

Індекс елемента, або \*\*`false`\*\*якщо значення не знайдено.

> **Зауваження**
> 
> Елементи порівнюються строго, за типом та значенням.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::find()****

```php
<?php
$sequence = new \Ds\Vector(["a", 1, true]);

var_dump($sequence->find("a")); // 0
var_dump($sequence->find("b")); // false
var_dump($sequence->find("1")); // false
var_dump($sequence->find(1));   // 1
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
bool(false)
bool(false)
int(1)
```