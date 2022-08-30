Повертає результат застосування callback-функції до всіх значень двосторонньої черги

-   [« DsDeque::last](ds-deque.last.html)
    
-   [ДсDeque::merge »](ds-deque.merge.html)
    
-   [PHP Manual](index.md)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Повертає результат застосування callback-функції до всіх значень двосторонньої черги
    

# ДсDeque::map

(PECL ds >= 1.0.0)

ДсDeque::map — Повертає результат застосування callback-функції до всіх значень двосторонньої черги

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

Аргумент типу [callable](language.types.callable.md)

Ця функція повинна повертати нове значення для кожного елемента двосторонньої черги.

### Значення, що повертаються

Результат застосування `callback`функції до кожного значення двосторонньої черги.

> **Зауваження**
> 
> Значення поточної двосторонньої черги залишаться незмінними.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::map()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);

print_r($deque->map(function($value) { return $value * 2; }));
print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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