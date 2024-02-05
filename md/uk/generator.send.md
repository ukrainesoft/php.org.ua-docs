---
navigation:
  - generator.rewind.md: '« Generator::rewind'
  - generator.throw.md: 'Generator::throw »'
  - index.md: PHP Manual
  - class.generator.md: Generator
title: 'Generator::send'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Generator::send

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

Generator::send — Передати значення в генератор

### Опис

```methodsynopsis
public Generator::send(mixed $value): mixed
```

Передача заданого значення в генератор як результат поточного виразу [yield](language.generators.syntax.md#control-structures.yield) та поновлення його роботи.

Якщо генератор ще не дійшов до першого виклику оператора [yield](language.generators.syntax.md#control-structures.yield), він виконається до моменту першого виклику [yield](language.generators.syntax.md#control-structures.yield), Перш ніж передасть у нього значення. Так що немає необхідності викликати генератор за допомогою [Generator::next()](generator.next.md) перед викликом цього методу (як це робиться в Python).

### Список параметрів

`value`

Значення, що відправляється в генератор. Це значення буде поточним значенням виразу, що повертається [yield](language.generators.syntax.md#control-structures.yield)генератора.

### Значення, що повертаються

Повертає згенероване значення.

### Приклади

**Пример #1 Использование**Generator::send()**для внедрения значений**

```php
<?php
function printer() {
    echo "I'm printer!".PHP_EOL;
    while (true) {
        $string = yield;
        echo $string.PHP_EOL;
    }
}

$printer = printer();
$printer->send('Hello world!');
$printer->send('Bye world!');
?>
```

Результат виконання наведеного прикладу:

```
I'm printer!
Hello world!
Bye world!
```
