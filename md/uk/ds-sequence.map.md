Повертає результат застосування callback-функції до всіх значень колекції

-   [« DsSequence::last](ds-sequence.last.html)
    
-   [ДсSequence::merge »](ds-sequence.merge.html)
    
-   [PHP Manual](index.md)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Повертає результат застосування callback-функції до всіх значень колекції
    

# ДсSequence::map

(PECL ds >= 1.0.0)

ДсSequence::map — Повертає результат застосування callback-функції до всіх значень колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::map(callable $callback): Ds\Sequence
```

Повертає результат застосування callback-функції, переданої в `callback`до всіх значень колекції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Аргумент типу [callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента колекції.

### Значення, що повертаються

Результат застосування `callback` до кожного значення колекції.

> **Зауваження**
> 
> Значення поточної колекції залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::map()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

print_r($sequence->map(function($value) { return $value * 2; }));
print_r($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
Ds\Vector Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
```