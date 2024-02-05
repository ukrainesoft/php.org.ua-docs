---
navigation:
  - random-engine-xoshiro256starstar.jump.md: '« Random\\Engine\\Xoshiro256StarStar::jump'
  - random-engine-xoshiro256starstar.serialize.md: 'Random\\Engine\\Xoshiro256StarStar::\_\_serialize »'
  - index.md: PHP Manual
  - class.random-engine-xoshiro256starstar.md: Random\\Engine\\Xoshiro256StarStar
title: 'Random\\Engine\\Xoshiro256StarStar::jumpLong'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\Xoshiro256StarStar::jumpLong

(PHP 8 >= 8.2.0)

Random\\Engine\\Xoshiro256StarStar::jumpLong - Ефективно переміщає двигун вперед на 2^192 кроки

### Опис

```methodsynopsis
public Random\Engine\Xoshiro256StarStar::jumpLong(): void
```

Переміщає стан алгоритму вперед на 2192 кроки, якби метод [Random\\Engine\\Xoshiro256StarStar::generate()](random-engine-xoshiro256starstar.generate.md) був викликаний 2192 рази.

Мета способу - полегшити створення нового движка [Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md)из существующего заполненного движка[Random\\Engine\\Xoshiro256StarStar](class.random-engine-xoshiro256starstar.md). Заданий двигун діє як проект, який можна [клонувати](language.oop5.cloning.md) і повторно використовувати для створення 264 послідовностей, що не перетинаються, з 2192 значеннями кожна.

Метод може бути поєднаний з [Random\\Engine\\Xoshiro256StarStar::jump()](random-engine-xoshiro256starstar.jump.md) для подальшого поділу кожної з 264 послідовностей, згенерованих даним методом, на 264 послідовності по 2128 значення кожна.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Random\\Engine\\Xoshiro256StarStar::jumpLong()\*\*\*\*

```php
<?php
$blueprintRng = new \Random\Engine\Xoshiro256StarStar(0);

// У каждого родительского движка свой собственный блок из 2**192 значений.
$parent1 = clone $blueprintRng;
$blueprintRng->jumpLong();

$parent2 = clone $blueprintRng;
$blueprintRng->jumpLong();

// У каждого из дочерних движков свой собственный блок из 2**128 значений,
взятый из блока 2**192 значений их родительского движка.
$child1a = clone $parent1;
$parent1->jump();
$child1b = clone $parent1;
$parent1->jump();

$child2a = clone $parent2;
$parent2->jump();
$child2b = clone $parent2;
$parent2->jump();

echo "Дочерний 1A: ", bin2hex($child1a->generate()), "\n";
echo "Дочерний 1B: ", bin2hex($child1b->generate()), "\n";
echo "Дочерний 2A: ", bin2hex($child2a->generate()), "\n";
echo "Дочерний 2B: ", bin2hex($child2b->generate()), "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Дочерний 1A: b4f275cb365fec99
Дочерний 1B: 2cd646c8ed156237
Дочерний 2A: eb3729a722a504e7
Дочерний 2B: d4208dc85bdd6dc3
```

### Дивіться також

-   [Random\\Engine\\Xoshiro256StarStar::jump()](random-engine-xoshiro256starstar.jump.md) \- Ефективно переміщає двигун вперед на 2^128 кроків
