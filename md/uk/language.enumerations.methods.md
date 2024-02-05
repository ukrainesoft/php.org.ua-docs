---
navigation:
  - language.enumerations.backed.md: Типізовані перерахування
  - language.enumerations.static-methods.md: Статичні методи перерахувань »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Методи перерахувань
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Методи перерахувань

Перерахування (як чисті, і типизированные) можуть містити методи і можуть реалізовувати інтерфейси. Якщо перерахування реалізує інтерфейс, то будь-яка перевірка типу цього інтерфейсу також прийме всі варіанти цього перерахування.

```php
<?php

interface Colorful
{
    public function color(): string;
}

enum Suit implements Colorful
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;

    // Выполняет контракт интерфейса.
    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }

    // Не часть интерфейса; хорошо.
    public function shape(): string
    {
        return "Rectangle";
    }
}

function paint(Colorful $c)
{
   /* ... */
}

paint(Suit::Clubs);  // Работает

print Suit::Diamonds->shape(); // выведет "Rectangle"
?>
```

У цьому прикладі кожен із чотирьох екземплярів `Suit`имеет два метода:`color()`и`shape()`. У коді, що викликає, і при перевірці типів екземпляри перерахування поводяться точно так само, як і будь-який інший екземпляр об'єкта.

У типізованих переліках оголошення інтерфейсу відбувається після оголошення типу перерахунку.

```php
<?php

interface Colorful
{
    public function color(): string;
}

enum Suit: string implements Colorful
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';

    // Выполняет интерфейсный контракт.
    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }
}
?>
```

Переменная`$this` визначено всередині методу і посилається на екземпляр варіанта.

Складність методів у перерахування не обмежена, але на практиці методи перерахувань частіше повертають статичне значення або результат обробки змінної `$this` виразом [match](control-structures.match.md)щоб результати обробки окремих екземплярів перерахування відрізнялися.

Зверніть увагу, у цьому прикладі кращою практикою побудови даних було б визначити тип перерахування `SuitColor` зі значеннями Red та Black і повертати їх замість рядкових літералів. Однак це ускладнило б приклад.

Ієрархія в прикладі логічно схожа на наступну структуру класів (хоча це не справжній код, що виконується):

```php
<?php

interface Colorful
{
    public function color(): string;
}

final class Suit implements UnitEnum, Colorful
{
    public const Hearts = new self('Hearts');
    public const Diamonds = new self('Diamonds');
    public const Clubs = new self('Clubs');
    public const Spades = new self('Spades');

    private function __construct(public readonly string $name) {}

    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }

    public function shape(): string
    {
        return "Прямоугольник";
    }

    public static function cases(): array
    {
        // Недопустимый метод, поскольку определение метода cases() в перечислениях вручную запрещено.
        // Смотрите также раздел "Список значений".
    }
}
?>
```

У переліках дозволено оголошувати загальнодоступні, закриті та захищені методи, хоча на практиці закриті та захищені методи еквівалентні, оскільки успадкування не дозволене.
