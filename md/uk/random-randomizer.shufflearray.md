---
navigation:
  - random-randomizer.serialize.md: '« Random\\Randomizer::\_\_serialize'
  - random-randomizer.shufflebytes.md: 'Random\\Randomizer::shuffleBytes »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::shuffleArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::shuffleArray

(PHP 8 >= 8.2.0)

Random\\Randomizer::shuffleArray — Отримує перестановку масиву

### Опис

```methodsynopsis
public Random\Randomizer::shuffleArray(array $array): array
```

Повертає рівномірно обрану перестановку вхідного масиву `array`

Кожна можлива перестановка вхідного масиву `array` з рівною ймовірністю буде повернуто.

### Список параметрів

`array`

Масив (array), значення якого перемішуються.

Вхідний масив (array) не буде змінено.

### Значення, що повертаються

Перестановка значений параметра`array`

Ключі вхідного масиву `array` не зберігаються; повертається масив (array) буде списком ([array\_is\_list()](function.array-is-list.md)

### Помилки

-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Приклад #1 Приклад використання** Random\\Randomizer::shuffleArray()\*\*\*\*

```php
<?php
$r = new \Random\Randomizer();

$fruits = [ 'red' => '🍎', 'green' => '🥝', 'yellow' => '🍌', 'pink' => '🍑', 'purple' => '🍇' ];

// Перемешивание массива:
echo "Салат: ", implode(', ', $r->shuffleArray($fruits)), "\n";

// Перемешивание массива ещё раз:
echo "Другой салат: ", implode(', ', $r->shuffleArray($fruits)), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Салат: 🍎, 🥝, 🍇, 🍌, 🍑
Другой салат: 🍑, 🍇, 🥝, 🍎, 🍌
```
