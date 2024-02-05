---
navigation:
  - ds-vector.count.md: '« Ds\\Vector::count'
  - ds-vector.find.md: 'Ds\\Vector::find »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::filter

(PECL ds >= 1.0.0)

Ds\\Vector::filter — Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Vector::filter(callable $callback = ?): Ds\Vector
```

Створює новий вектор із елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`**(смотрите[приведення до boolean](language.types.boolean.md#language.types.boolean.casting)

### Значення, що повертаються

Новий вектор, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback`не задан.

### Приклади

**Приклад #1 Приклад**Ds\\Vector::filter()**с использованием callback-функции**

```php
<?php
$vector = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($vector->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Vector)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад**Ds\\Vector::filter()\*\* без callback-функції\*\*

```php
<?php
$vector = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($vector->filter());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Vector)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```
