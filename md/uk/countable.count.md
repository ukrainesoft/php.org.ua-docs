---
navigation:
  - class.countable.html: « Countable
  - class.outeriterator.html: OuterIterator »
  - index.html: PHP Manual
  - class.countable.html: Countable
title: 'Countable::count'
---
# Countable::count

(PHP 5> = 5.1.0, PHP 7, PHP 8)

Countable::count — Кількість елементів об'єкта

### Опис

```methodsynopsis
public Countable::count(): int
```

Цей метод виконується під час використання [count()](function.count.html) на об'єкті, що реалізує інтерфейс [Countable](class.countable.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення користувача типу int.

> **Зауваження**
> 
> Значення, що повертається, наводиться до типу int.

### Приклади

**Приклад #1 Приклад використання **Countable::count()****

```php
<?php
class myCounter implements Countable {
    private $count = 0;
    public function count() {
        return ++$this->count;
    }
}

$counter = new myCounter;

for($i=0; $i<10; ++$i) {
    echo "Я посчитан " . count($counter) . " раз\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

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
