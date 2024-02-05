---
navigation:
  - language.enumerations.traits.md: « Трейти
  - language.enumerations.object-differences.md: Відмінності від об'єктів »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Значення перерахування у постійних виразах
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Значення перерахування у постійних виразах

Оскільки в самому перерахуванні варіанти оголошені константами, їх можна використовувати як статичні значення в більшій частині константних виразів: значення за промовчанням для властивостей, значення за промовчанням для статичних змінних, значення за промовчанням для параметрів, глобальні значення та значення констант класу. Їх не можна вказувати як значення в інших варіантах перерахування, але стандартні константи можуть посилатися на варіант перерахування.

Однак неявні виклики магічних методів, як це відбувається під час реалізації інтерфейсу [ArrayAccess](class.arrayaccess.md) у перерахуваннях, — не допускаються у статичних чи константних визначеннях, оскільки неможливо абсолютно гарантувати, що результуюче значення буде детермінованим чи виклик виклику методу не матиме побічних ефектів. Виклики функцій, виклики методів та доступ до властивостей, як і раніше, неприпустимі у постійних виразах.

```php
<?php

// Это полностью законное определение перечисления.
enum Direction implements ArrayAccess
{
    case Up;
    case Down;

    public function offsetExists($offset): bool
    {
        return false;
    }

    public function offsetGet($offset): mixed
    {
        return null;
    }

    public function offsetSet($offset, $value): void
    {
        throw new Exception();
    }

    public function offsetUnset($offset): void
    {
        throw new Exception();
    }
}

class Foo
{
    // Это разрешено.
    const DOWN = Direction::Down;

    // Это запрещено, так как не может быть детерминированным.
    const UP = Direction::Up['short'];
    // Fatal error: Cannot use [] on enums in constant expression
}

// Это совершенно законно, потому что это не постоянное выражение.
$x = Direction::Up['short'];
var_dump("\$x – это " . var_export($x, true));

$foo = new Foo();
?>
```
