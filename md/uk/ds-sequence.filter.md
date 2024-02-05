---
navigation:
  - ds-sequence.contains.md: '« Ds\\Sequence::contains'
  - ds-sequence.find.md: 'Ds\\Sequence::find »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::filter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::filter

(PECL ds >= 1.0.0)

Ds\\Sequence::filter — Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції

### Опис

```methodsynopsis
abstract public Ds\Sequence::filter(callable $callback = ?): Ds\Sequence
```

Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції.

### Список параметрів

`callback`

```methodsynopsis
callback(mixed $value): bool
```

Необов'язковий аргумент типу [callable](language.types.callable.md), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`**(смотри[приведення до boolean](language.types.boolean.md#language.types.boolean.casting)

### Значення, що повертаються

Нова послідовність, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback`не задан.

### Приклади

**Пример #1 Пример использования**Ds\\Sequence::filter()**с callback-функцией**

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($sequence->filter(function($value) {
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

**Пример #2 Пример использования**Ds\\Sequence::filter()\*\* без callback-функції\*\*

```php
<?php
$sequence = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($sequence->filter());
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
