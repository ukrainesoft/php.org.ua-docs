---
navigation:
  - limititerator.current.md: '« LimitIterator::current'
  - limititerator.key.md: 'LimitIterator::key »'
  - index.md: PHP Manual
  - class.limititerator.md: LimitIterator
title: 'LimitIterator::getPosition'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LimitIterator::getPosition

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

LimitIterator::getPosition — Повертає поточну позицію

### Опис

```methodsynopsis
public LimitIterator::getPosition(): int
```

Повертає поточну позицію (починаючи з 0) внутрішнього об'єкта-ітератора [Iterator](class.iterator.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна позиція.

### Приклади

**Пример #1 Пример использования**LimitIterator::getPosition()\*\*\*\*

```php
<?php
$fruits = array(
    'a' => 'apple',
    'b' => 'banana',
    'c' => 'cherry',
    'd' => 'damson',
    'e' => 'elderberry'
);
$array_it = new ArrayIterator($fruits);
$limit_it = new LimitIterator($array_it, 2, 3);
foreach ($limit_it as $item) {
    echo $limit_it->getPosition() . ' ' . $item . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
2 cherry
3 damson
4 elderberry
```

### Дивіться також

-   [FilterIterator::key()](filteriterator.key.md) \- Отримує поточний ключ
