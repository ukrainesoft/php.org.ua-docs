---
navigation:
  - ds-deque.clear.md: '« Ds\\Deque::clear'
  - ds-deque.contains.md: 'Ds\\Deque::contains »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Deque::\_\_construct — Створює новий екземпляр

### Опис

public**Ds\\Deque::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::\_\_construct()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque();
var_dump($deque);

$deque = new \Ds\Deque([1, 2, 3]);
var_dump($deque);
?>
```

Висновок наведеного прикладу буде схожим на:

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
