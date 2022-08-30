Повертає поверхневу копію колекції

-   [« DsDeque::contains](ds-deque.contains.html)
    
-   [ДсDeque::count »](ds-deque.count.html)
    
-   [PHP Manual](index.html)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Повертає поверхневу копію колекції
    

# ДсDeque::copy

(PECL ds >= 1.0.0)

ДсDeque::copy — Повертає поверхневу копію колекції

### Опис

```methodsynopsis
public Ds\Deque::copy(): Ds\Deque
```

Повертає поверхневу копію двосторонньої черги.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поверхнева копія двосторонньої черги.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::copy()****

```php
<?php
$a = new \Ds\Deque([1, 2, 3]);
$b = $a->copy();

$b->push(4);

print_r($a);
print_r($b);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
)
Ds\Deque Object
(
    [0] => 1
    [1] => 2
    [2] => 3
    [3] => 4
)
```