---
navigation:
  - ds-set.diff.md: '« Ds\\Set::diff'
  - ds-set.first.md: 'Ds\\Set::first »'
  - index.md: PHP Manual
  - class.ds-set.md: Ds\\Set
title: 'Ds\\Set::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Set::filter

(PECL ds >= 1.0.0)

Ds\\Set::filter — Створює новий список з елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
public Ds\Set::filter(callable $callback = ?): Ds\Set
```

Створює новий набір елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Опціональний аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивитися [приведення до boolean](language.types.boolean.md#language.types.boolean.casting)

### Значення, що повертаються

Новий набір, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback`не задан.

### Приклади

**Пример #1 Пример**Ds\\Set::filter()**с использованием callback-функции**

```php
<?php
$set = new \Ds\Set([1, 2, 3, 4, 5]);

var_dump($set->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Пример #2 Пример**Ds\\Set::filter()\*\* без callback-функції\*\*

```php
<?php
$set = new \Ds\Set([0, 1, 'a', true, false]);

var_dump($set->filter());
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Set)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  string(1) "a"
  [2]=>
  bool(true)
}
```
