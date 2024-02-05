---
navigation:
  - ds-deque.last.md: '« Ds\\Deque::last'
  - ds-deque.merge.md: 'Ds\\Deque::merge »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::map'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::map

(PECL ds >= 1.0.0)

Ds\\Deque::map — Повертає результат застосування callback-функції до всіх значень двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::map(callable $callback): Ds\Deque
```

Повертає результат застосування callback-функції, переданої в `callback`до всіх значень двосторонньої черги.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Аргумент типа[callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента двосторонньої черги.

### Значення, що повертаються

Результат применения`callback`\-функції до кожного значення двосторонньої черги.

> **Зауваження** :
> 
> Значення поточної двосторонньої черги залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання** Ds\\Deque::map()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

print_r($deque->map(function($value) { return $value * 2; }));
print_r($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Ds\Deque Object
(
    [0] => 2
    [1] => 4
    [2] => 6
)
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
```
