---
navigation:
  - random-randomizer.getint.md: '« Random\\Randomizer::getInt'
  - random-randomizer.nextint.md: 'Random\\Randomizer::nextInt »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::nextFloat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::nextFloat

(PHP 8 >= 8.3.0)

Random\\Randomizer::nextFloat — Отримує число з точкою, що плаває, з відкритого праворуч інтервалу \[

### Опис

```methodsynopsis
public Random\Randomizer::nextFloat(): float
```

Повертає рівномірно обране рівнорозподілене число з плаваючою точкою з відкритого праворуч інтервалу від `0.0`до`1.0`але не включаючи саму одиницю.

Імовірність того, що повернене число з плаваючою точкою виявиться в межах заданого відкритого праворуч підінтервалу пропорційна розміру підінтервалу. Тобто ймовірність того, що число з плаваючою точкою буде *менше* `0.5`, дорівнює 50%, що дорівнює ймовірності того, що число з плаваючою точкою буде *не менше* `0.5`. Аналогічно, ймовірність того, що число з точкою, що плаває, опиниться в межах відкритого праворуч інтервалу від `0.2`до`0.25`, Не включаючи останнє значення, - дорівнює 5%.

Ця властивість робить метод **Random\\Randomizer::nextFloat()** простим засобом для генерації випадкового логічного значення із заданою ймовірністю, перевіряючи, *чи менше* число, що повертається з плаваючою точкою заданої ймовірності.

> **Зауваження** :
> 
> Область визначення методів, що повертаються. **Random\\Randomizer::nextFloat()** чисел з плаваючою точкою ідентична області визначення методу, викликаного з аргументами `Randomizer::getFloat(0.0, 1.0, IntervalBoundary::ClosedOpen)`
> 
> Внутренняя реализация метода**Random\\Randomizer::nextFloat()** ефективніша.

**Застереження**

Масштабування значення, що повертається до іншого інтервалу через множення або додавання (т. н. афінне перетворення) іноді призводить до зміщення результуючого значення оскільки числа з плаваючою точкою не однаково щільні по числовій прямій. Оскільки не всі значення можуть бути точно представлені числом з плаваючою точкою, результат афінного перетворення іноді повертає значення за межами запитаного інтервалу через неявне округлення . [Детальне пояснення](random-randomizer.getfloat.md#random-randomizer.getfloat.affine-transformation) проблем, пов'язаних з афінним перетворенням, дано в документації до методу [Random\\Randomizer::getFloat()](random-randomizer.getfloat.md)

Для генерації випадкового числа з плаваючою точкою в довільному інтервалі краще віддати перевагу методу [Random\\Randomizer::getFloat()](random-randomizer.getfloat.md). Для генерації випадкового цілого числа у довільному інтервалі користуються методом [Random\\Randomizer::getInt()](random-randomizer.getint.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рівномірно обране, рівнорозподілене число з плаваючою точкою з відкритого праворуч (`IntervalBoundary::ClosedOpen`) інтервалу \[0.0, 1.0). Значение`0.0` — можливе значення, що повертається, значення `1.0` - Ні.

### Помилки

-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Приклад #1 Приклад использования метода**Random\\Randomizer::nextFloat()\*\*\*\*

```php
<?php

$r = new \Random\Randomizer();

// Результирующее логическое значение будет истинным с равной вероятностью.
$chance = 0.5;

$bool = $r->nextFloat() < $chance;

echo ($bool ? "Вы выиграли" : "Вы проиграли"), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
You won
```

**Приклад #2 Неправильне масштабування через афінне перетворення**

```php
<?php

final class MaxEngine implements Random\Engine {
    public function generate(): string {
        return "\xff";
    }
}

$randomizer = new \Random\Randomizer(new MaxEngine);

$min = 3.5;
$max = 4.5;

// НЕ ДЕЛАЙТЕ ЭТОГО:
//
// Это выведет значение 4.5, несмотря на выборку метода nextFloat()
// из открытого справа интервала, который никогда не вернёт значение 1.
printf("Неправильное масштабирование: %.17g", $randomizer->nextFloat() * ($max - $min) + $min);

// Правильно:
// $randomizer->getFloat($min, $max, \Random\IntervalBoundary::ClosedOpen);
?>
```

Результат виконання наведеного прикладу:

```
Неправильное масштабирование: 4.5
```

### Дивіться також

-   [Random\\Randomizer::getFloat()](random-randomizer.getfloat.md) \- Отримує рівномірно обране число з плаваючою точкою
