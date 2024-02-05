---
navigation:
  - ds-queue.clear.md: '« Ds\\Queue::clear'
  - ds-queue.copy.md: 'Ds\\Queue::copy »'
  - index.md: PHP Manual
  - class.ds-queue.md: Ds\\Queue
title: 'Ds\\Queue::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Queue::\_\_construct

(PECL ds >= 1.0.0)

Ds\\Queue::\_\_construct — Створює новий екземпляр

### Опис

public **Ds\\Queue::\_\_construct** [mixed](language.types.declarations.md#language.types.declarations.mixed) `$values`

Створює новий екземпляр, використовуючи або об'єкт, що реалізує [traversable](class.traversable.md), або масив, передані як параметр `values`

### Список параметрів

`values`

Об'єкт, що реалізує інтерфейс traversable або масив.

### Приклади

**Приклад #1 Приклад використання** Ds\\Queue::\_\_construct()\*\*\*\*

```php
<?php
$queue = new \Ds\Queue();
var_dump($queue);


$queue = new \Ds\Queue([1, 2, 3]);
var_dump($queue);
?>
```

Висновок наведеного прикладу буде схожим на:

```
object(Ds\Queue)#2 (0) {
}
object(Ds\Queue)#2 (3) {
  [0]=>
  int(1)
  [1]=>
  int(2)
  [2]=>
  int(3)
}
```
