---
navigation:
  - ds-deque.count.md: '« Ds\\Deque::count'
  - ds-deque.find.md: 'Ds\\Deque::find »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::filter

(PECL ds >= 1.0.0)

Ds\\Deque::filter — Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Deque::filter(callable $callback = ?): Ds\Deque
```

Створює нову двосторонню чергу з елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`**(смотрите[приведення до boolean](language.types.boolean.md#language.types.boolean.casting)

### Значення, що повертаються

Нова двостороння черга, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback`не задан.

### Приклади

**Приклад #1 Приклад**Ds\\Deque::filter()**с использованием callback-функции**

```php
<?php
$deque = new \Ds\Deque([1, 2, 3, 4, 5]);

var_dump($deque->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Deque)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад**Ds\\Deque::filter()\*\* без callback-функції\*\*

```php
<?php
$deque = new \Ds\Deque([0, 1, 'a', true, false]);

var_dump($deque->filter());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Deque)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```
