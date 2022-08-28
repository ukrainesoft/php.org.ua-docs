Методи перерахувань

-   [« Типизированные перечисления](language.enumerations.backed.html)
    
-   [Статические методы перечислений »](language.enumerations.static-methods.html)
    
-   [PHP Manual](index.html)
    
-   [Перечисления](language.enumerations.html)
    
-   Методи перерахувань
    

## Методи перерахувань

Перерахування (як чисті перерахування, і типизированные перерахування) можуть містити методи і можуть реалізовувати інтерфейси. Якщо перерахування реалізує інтерфейс, то будь-яка перевірка типу цього інтерфейсу також прийматиме всі варіанти цього перерахування.

```php
<?php

interface Colorful
{
    public function color(): string;
}

enum Suit implements Colorful
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;

    // Выполняет интерфейсный контракт.
    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }

    // Не является частью интерфейса; хорошо.
    public function shape(): string
    {
        return "Rectangle";
    }
}

function paint(Colorful $c) { ... }

paint(Suit::Clubs);  // Работает

print Suit::Diamonds->shape(); // выведет "Rectangle"
?>
```

У цьому прикладі у всіх чотирьох екземплярів `Suit` є два методи: `color()` і `shape()`. Що стосується коду, що викликає, і перевірки типів, вони поводяться точно так само, як і будь-який інший екземпляр об'єкта.

У типізованих переліках оголошення інтерфейсу відбувається після оголошення типу.

```php
<?php
interface Colorful
{
    public function color(): string;
}

enum Suit: string implements Colorful
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';

    // Выполняет интерфейсный контракт.
    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }
}
?>
```

Усередині методу визначається змінна `$this`, Що посилається на екземпляр варіанта.

Методи можуть бути як завгодно складними, але на практиці зазвичай повертають статичне значення або [match](control-structures.match.html) для `$this`, щоб надати різні результати для різних випадків.

Зверніть увагу, що в цьому випадку було б краще визначити тип перерахування `SuitColor` зі значеннями Red і Black і повернути його натомість. Однак це ускладнило б цей приклад.

Вищезгадана ієрархія логічно схожа на наступну структуру класів (хоча це не фактичний код, що виконується):

```php
<?php
interface Colorful
{
    public function color(): string;
}

final class Suit implements UnitEnum, Colorful
{
    public const Hearts = new self('Hearts');
    public const Diamonds = new self('Diamonds');
    public const Clubs = new self('Clubs');
    public const Spades = new self('Spades');

    private function __construct(public readonly string $name) {}

    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный'
        };
    }

    public function shape(): string
    {
        return "Прямоугольник";
    }

    public static function cases(): array
    {
        // Недопустимый метод, поскольку определение метода cases() в перечислениях вручную запрещено.
        // Смотрите также раздел "Список значений".
    }
}
?>
```

Методи можуть бути загальнодоступними, закритими або захищеними, хоча на практиці закриті та захищені еквівалентні, оскільки успадкування не допускається.