Зменшує колекцію до одного значення, використовуючи callback-функцію

-   [« DsMap::putAll](ds-map.putall.html)
    
-   [ДсMap::remove »](ds-map.remove.html)
    
-   [PHP Manual](index.md)
    
-   [Коллекция пар ключ-значение](class.ds-map.html)
    
-   Зменшує колекцію до одного значення, використовуючи callback-функцію
    

# ДсMap::reduce

(PECL ds >= 1.0.0)

ДсMap::reduce — Зменшує колекцію до одного значення, використовуючи callback-функцію

### Опис

```methodsynopsis
public Ds\Map::reduce(callable $callback, mixed $initial = ?): mixed
```

Зменшує колекцію до одного значення, використовуючи callback-функцію.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $carry, mixed $key, mixed $value): mixed
```

`carry`

Значення, повернене попереднім запуском функції або `initial`, якщо функцію запущено вперше.

`key`

Ключ поточної ітерації.

`value`

Значення поточної ітерації.

`initial`

Початкове значення для параметра carry. Можна вказати **`null`**

### Значення, що повертаються

Значення, повернене остаточним запуском callback-функції.

### Приклади

**Приклад #1 Приклад використання **ДсMap::reduce()** з початковим значенням**

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

$callback = function($carry, $key, $value) {
    return $carry * $value;
};

var_dump($map->reduce($callback, 5));

// Итерации:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(30)
```

**Приклад #2 Приклад використання **ДсMap::reduce()** без початкового значення**

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->reduce(function($carry, $key, $value) {
    return $carry + $value + 5;
}));

// Итерации:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(21)
```