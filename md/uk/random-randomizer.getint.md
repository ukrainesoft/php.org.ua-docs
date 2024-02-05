---
navigation:
  - random-randomizer.getfloat.md: '« Random\\Randomizer::getFloat'
  - random-randomizer.nextfloat.md: 'Random\\Randomizer::nextFloat »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::getInt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::getInt

(PHP 8 >= 8.2.0)

Random\\Randomizer::getInt — Отримує рівномірно вибране ціле число

### Опис

```methodsynopsis
public Random\Randomizer::getInt(int $min, int $max): int
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`min`

Найменше значення, що повертається.

`max`

Найбільше значення, що повертається.

### Значення, що повертаються

Повертає рівномірно обране ціле число із замкнутого інтервалу \[`min` `max`\]. Можливими значеннями, що повертаються, є як `min`, так и`max`

### Помилки

-   Якщо `max`менше ніж`min`, буде викинута помилка [ValueError](class.valueerror.md)
-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Пример #1 Пример использования**Random\\Randomizer::getInt()\*\*\*\*

```php
<?php
$r = new \Random\Randomizer();

// Случайное целое число в диапазоне:
echo $r->getInt(1, 100), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
...
```

### Дивіться також

-   [random\_int()](function.random-int.md) \- Отримує криптографічно безпечне, рівномірно вибране ціле число
-   [Random\\Randomizer::getFloat()](random-randomizer.getfloat.md) \- Отримує рівномірно обране число з плаваючою точкою
