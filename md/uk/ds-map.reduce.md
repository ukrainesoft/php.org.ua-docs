---
navigation:
  - ds-map.putall.md: '« Ds\\Map::putAll'
  - ds-map.remove.md: 'Ds\\Map::remove »'
  - index.md: PHP Manual
  - class.ds-map.md: Ds\\Map
title: 'Ds\\Map::reduce'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Map::reduce

(PECL ds >= 1.0.0)

Ds\\Map::reduce — Зменшує колекцію до одного значення, використовуючи callback-функцію

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

**Приклад #1 Приклад використання** Ds\\Map::reduce()\*\* з початковим значенням\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

$callback = function($carry, $key, $value) {
    return $carry * $value;
};

var_dump($map->reduce($callback, 5));

// Итерации:
//
// $carry = $initial = 5
//
// $carry = $carry * 1 =  5
// $carry = $carry * 2 = 10
// $carry = $carry * 3 = 30
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(30)
```

**Приклад #2 Приклад використання** Ds\\Map::reduce()\*\* без початкового значення\*\*

```php
<?php
$map = new \Ds\Map(["a" => 1, "b" => 2, "c" => 3]);

var_dump($map->reduce(function($carry, $key, $value) {
    return $carry + $value + 5;
}));

// Итерации:
//
// $carry = $initial = null
//
// $carry = $carry + 1 + 5 =  6
// $carry = $carry + 2 + 5 = 13
// $carry = $carry + 3 + 5 = 21
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(21)
```
