---
navigation:
  - class.countable.md: « Countable
  - class.outeriterator.md: OuterIterator »
  - index.md: PHP Manual
  - class.countable.md: Countable
title: 'Countable::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Countable::count

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

Countable::count — Кількість елементів об'єкта

### Опис

```methodsynopsis
public Countable::count(): int
```

Цей метод виконується під час використання [count()](function.count.md) на об'єкті, що реалізує інтерфейс [Countable](class.countable.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення користувача типу int.

> **Зауваження** :
> 
> Значення, що повертається, наводиться до типу int.

### Приклади

**Приклад #1 Приклад використання** Countable::count()\*\*\*\*

```php
<?php
class myCounter implements Countable {
    private $count = 0;
    public function count() {
        return ++$this->count;
    }
}

$counter = new myCounter;

for($i=0; $i<10; ++$i) {
    echo "Я посчитан " . count($counter) . " раз\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Я посчитан 1 раз
Я посчитан 2 раз
Я посчитан 3 раз
Я посчитан 4 раз
Я посчитан 5 раз
Я посчитан 6 раз
Я посчитан 7 раз
Я посчитан 8 раз
Я посчитан 9 раз
Я посчитан 10 раз
```
