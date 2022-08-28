Повертає результат додавання всіх заданих значень до колекції

-   [« Ds\\Sequence::map](ds-sequence.map.html)
    
-   [Ds\\Sequence::pop »](ds-sequence.pop.html)
    
-   [PHP Manual](index.html)
    
-   [Последовательность](class.ds-sequence.html)
    
-   Повертає результат додавання всіх заданих значень до колекції
    

# ДсSequence::merge

(PECL ds >= 1.0.0)

ДсSequence::merge — Повертає результат додавання всіх заданих значень до колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::merge(mixed $values): Ds\Sequence
```

Повертає результат додавання всіх заданих значень до колекції.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.html) або array.

### Значення, що повертаються

Результат додавання всіх переданих значень до колекції. Фактично робиться копія колекції, до якої додаються значення.

> **Зауваження**
> 
> Поточний екземпляр колекції залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::merge()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->merge([4, 5, 6]));
var_dump($sequence);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#2 (6) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
  [3]=>
  int(4)
  [4]=>
  int(5)
  [5]=>
  int(6)
}
object(Ds\Vector)#1 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```