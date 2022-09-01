---
navigation:
  - ds-sequence.contains.html: '« DsSequence::contains'
  - ds-sequence.find.html: 'ДсSequence::find »'
  - index.html: PHP Manual
  - class.ds-sequence.html: Послідовність
title: 'ДсSequence::filter'
---
# ДсSequence::filter

(PECL ds >= 1.0.0)

ДсSequence::filter — Створює нову послідовність елементів, вибраних за допомогою заданої callback-функції

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

Необов'язковий аргумент типу [callable](language.types.callable.html), який повертає **`true`**, якщо значення має бути включено та **`false`**, якщо ні.

Якщо callback-функція не задана, будуть включені тільки елементи, які призводять до логічного значення **`true`** (дивися [приведение к boolean](language.types.boolean.html#language.types.boolean.casting)

### Значення, що повертаються

Нова послідовність, що містить значення, для яких функція `callback` повернула **`true`**, або всі елементи, які при приведенні до логічного типу стають **`true`**, якщо параметр `callback` не заданий.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::filter()** з callback-функцією**

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3, 4, 5]);

var_dump($sequence->filter(function($value) {
    return $value % 2 == 0;
}));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#3 (2) {
  [0]=>
  int(2)
  [1]=>
  int(4)
}
```

**Приклад #2 Приклад використання **ДсSequence::filter()** без callback-функції**

```php
<?php
$sequence = new \Ds\Vector([0, 1, 'a', true, false]);

var_dump($sequence->filter());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
