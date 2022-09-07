---
navigation:
  - ds-deque.clear.md: '« DsDeque::clear'
  - ds-deque.contains.md: 'ДсDeque::contains »'
  - index.md: PHP Manual
  - class.ds-deque.md: Двостороння черга
title: 'ДсDeque::construct'
---
# ДсDeque::construct

(PECL ds >= 1.0.0)

ДсDeque::construct — Створює новий екземпляр

### Опис

public **ДсDeque::construct**[mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::construct()****

```php
<?php
$deque = new \Ds\Deque();
var_dump($deque);

$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Deque)#2 (0) {
}
object(Ds\Deque)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
