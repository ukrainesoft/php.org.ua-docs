---
navigation:
  - ds-deque.map.html: '« DsDeque::map'
  - ds-deque.pop.html: 'ДсDeque::pop »'
  - index.md: PHP Manual
  - class.ds-deque.html: Двостороння черга
title: 'ДсDeque::merge'
---
# ДсDeque::merge

(PECL ds >= 1.0.0)

ДсDeque::merge — Повертає результат додавання всіх заданих значень у двосторонню чергу

### Опис

```methodsynopsis
public Ds\Deque::merge(mixed $values): Ds\Deque
```

Повертає результат додавання всіх заданих значень двосторонню чергу.

### Список параметрів

`values`

Об'єкт класу [traversable](class.traversable.md) або array.

### Значення, що повертаються

Результат додавання всіх переданих значень у двосторонню чергу. Фактично робиться копія двосторонньої черги, до якої додаються значення.

> **Зауваження**
> 
> Поточний екземпляр двосторонньої черги залишиться недоторканим.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::merge()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

var_dump($deque->merge([4, 5, 6]));
var_dump($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Deque)#2 (6) {
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
object(Ds\Deque)#1 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
