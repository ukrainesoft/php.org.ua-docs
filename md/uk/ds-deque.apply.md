Оновлює всі значення, застосовуючи callback-функцію до кожного значення

-   [« DsDeque::allocate](ds-deque.allocate.html)
    
-   [ДсDeque::capacity »](ds-deque.capacity.html)
    
-   [PHP Manual](index.md)
    
-   [Двостороння черга](class.ds-deque.html)
    
-   Оновлює всі значення, застосовуючи callback-функцію до кожного значення
    

# ДсDeque::apply

(PECL ds >= 1.0.0)

ДсDeque::apply — Оновлює всі значення, застосовуючи callback-функцію до кожного значення

### Опис

```methodsynopsis
public Ds\Deque::apply(callable $callback): void
```

Оновлює всі значення, застосовуючи `callback`функцію до кожного значення.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): mixed
```

Об'єкт типу [callable](language.types.callable.md)

Callback-функція має повертати нове значення, яке замінить поточне.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::apply()****

```php
<?php
$deque = new \Ds\Deque([1, 2, 3]);
$deque->apply(function($value) { return $value * 2; });

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
```