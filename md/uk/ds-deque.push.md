Додає значення до кінця двосторонньої черги

-   [« DsDeque::pop](ds-deque.pop.html)
    
-   [ДсDeque::reduce »](ds-deque.reduce.html)
    
-   [PHP Manual](index.html)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Додає значення до кінця двосторонньої черги
    

# ДсDeque::push

(PECL ds >= 1.0.0)

ДсDeque::push — Додає значення до кінця двосторонньої черги

### Опис

```methodsynopsis
public Ds\Deque::push(mixed ...$values): void
```

Додає значення до кінця двосторонньої черги.

### Список параметрів

`values`

Значення, що додаються.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::push()****

```php
<?php
$deque = new \Ds\Deque();

$deque->push("a");
$deque->push("b");
$deque->push("c", "d");
$deque->push(...["e", "f"]);

print_r($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => a
    [1] => b
    [2] => c
    [3] => d
    [4] => e
    [5] => f
)
```