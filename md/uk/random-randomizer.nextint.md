---
navigation:
  - random-randomizer.nextfloat.md: '« Random\\Randomizer::nextFloat'
  - random-randomizer.pickarraykeys.md: 'Random\\Randomizer::pickArrayKeys »'
  - index.md: PHP Manual
  - class.random-randomizer.md: Random\\Randomizer
title: 'Random\\Randomizer::nextInt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Randomizer::nextInt

(PHP 8 >= 8.2.0)

Random\\Randomizer::nextInt — Отримує ціле позитивне число

### Опис

```methodsynopsis
public Random\Randomizer::nextInt(): int
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Позитивне ціле число від 0 до максимального значення, що залежить від кількості байт, що повертаються [Random\\Engine::generate()](random-engine.generate.md). Точне максимальне значення може бути розраховане як 2$engine\_bytes\*

### Помилки

-   Щоб уникнути невідповідностей, 32-бітовий PHP викидатиме виняток[Random\\RandomException](class.random-randomexception.md), якщо розмір значення, що повертається[Random\\Engine::generate()](random-engine.generate.md)перевищує 32 біти, тому що обране ціле число не може бути повернуто без втрат. Це стосується своїх 64-бітних двигунів[Random\\Engine\\PcgOneseq128XslRr64](class.random-engine-pcgoneseq128xslrr64.md) і [Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md). Будь-який користувальницький механізм, що повертає більше 4 байт випадкових даних, також піддається впливу.
-   Будь-які [Throwable](class.throwable.md), що викидаються методом[Random\\Engine::generate()](random-engine.generate.md)базового[`Random\Randomizer::$engine`](class.random-randomizer.md#random-randomizer.props.engine)

### Приклади

**Пример #1 Пример использования**Random\\Randomizer::nextInt()\*\*\*\*

```php
<?php
$r = new \Random\Randomizer();

// Случайное "следующее" целое число:
echo $r->nextInt(), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
8041689838856078718
```
