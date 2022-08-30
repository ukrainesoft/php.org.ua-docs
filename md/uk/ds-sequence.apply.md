Оновлення всіх значень застосуванням до них переданої callback-функції

-   [« DsSequence::allocate](ds-sequence.allocate.html)
    
-   [ДсSequence::capacity »](ds-sequence.capacity.html)
    
-   [PHP Manual](index.html)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Оновлення всіх значень застосуванням до них переданої callback-функції
    

# ДсSequence::apply

(PECL ds >= 1.0.0)

ДсSequence::apply — Оновлення всіх значень застосуванням до них переданої callback-функції

### Опис

```methodsynopsis
abstract public Ds\Sequence::apply(callable $callback): void
```

Оновлення всіх значень застосуванням до них переданої `callback`функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.html)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::apply()****

```php
<?php
$sequence = new \Ds\Sequence([1, 2, 3]);
$sequence->apply(function($value) { return $value * 2; });

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
```