---
navigation:
  - random-engine-xoshiro256starstar.generate.md: '« Random\\Engine\\Xoshiro256StarStar::generate'
  - random-engine-xoshiro256starstar.jumplong.md: 'Random\\Engine\\Xoshiro256StarStar::jumpLong »'
  - index.md: PHP Manual
  - class.random-engine-xoshiro256starstar.md: Random\\Engine\\Xoshiro256StarStar
title: 'Random\\Engine\\Xoshiro256StarStar::jump'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\Xoshiro256StarStar::jump

(PHP 8 >= 8.2.0)

Random\\Engine\\Xoshiro256StarStar::jump - Ефективно переміщає двигун вперед на 2^128 кроків

### Опис

```methodsynopsis
public Random\Engine\Xoshiro256StarStar::jump(): void
```

Переміщає стан алгоритму вперед на 2128 кроку, як метод [Random\\Engine\\Xoshiro256StarStar::generate()](random-engine-xoshiro256starstar.generate.md) був викликаний 2128 разів.

Мета способу - полегшити створення нового движка [Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md)из существующего заполненного движка[Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md). Заданий двигун діє як проект, який можна [клонувати](language.oop5.cloning.md) і повторно використовувати для створення 2128 послідовностей, що не перетинаються, з 2128 значеннями кожна.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** Random\\Engine\\Xoshiro256StarStar::jump()\*\*\*\*

```php
<?php
use Random\Engine\Xoshiro256StarStar;
use Random\Randomizer;

$blueprintRng = new Xoshiro256StarStar(0);

$fibers = [];
for ($i = 0; $i < 8; $i++) {
    $fiberRng = clone $blueprintRng;
    $blueprintRng->jump();

    $fiber = new Fiber(static function () use ($fiberRng, $i): void {
        $randomizer = new Randomizer($fiberRng);

        while (true) {
            Fiber::suspend();
            echo "{$i}: ", $randomizer->getInt(0, 100), "\n";
        }
    });
    $fiber->start();

    $fibers[] = $fiber;
}


// Даже если файберы выполняются в случайном порядке, они будут выводить одно и то же значение каждый раз,
// потому что у каждого из них свой собственный уникальный экземпляр RNG.
$randomizer = new Randomizer();

$fibers = $randomizer->shuffleArray($fibers);
foreach ($fibers as $fiber) {
    $fiber->resume();
}

$fibers = $randomizer->shuffleArray($fibers);
foreach ($fibers as $fiber) {
    $fiber->resume();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
4: 89
3: 10
2: 63
1: 75
6: 41
5: 56
0: 16
7: 60
7: 34
6: 58
1: 74
4: 63
3: 3
5: 42
2: 45
0: 86
```

### Дивіться також

-   [Random\\Engine\\Xoshiro256StarStar::jumpLong()](random-engine-xoshiro256starstar.jumplong.md) \- Ефективно переміщає двигун вперед на 2^192 кроки
