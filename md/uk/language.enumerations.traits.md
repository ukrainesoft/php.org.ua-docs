---
navigation:
  - language.enumerations.constants.html: « Константи перерахувань
  - language.enumerations.expressions.html: Значення перерахування у постійних виразах »
  - index.html: PHP Manual
  - language.enumerations.html: Перечисления
title: Трейти
---
## Трейти

Переліки можуть використовувати трейти, які будуть поводитися так само, як і класи. Застереження полягає в тому, що трейти, що використовуються (`use`) у перерахуванні не повинні містити властивостей. Вони можуть включати лише методи та статичні методи. Трейт із властивостями призведе до фатальної помилки.

```php
<?php
interface Colorful
{
    public function color(): string;
}

trait Rectangle
{
    public function shape(): string {
        return "Прямоугольние";
    }
}

enum Suit implements Colorful
{
    use Rectangle;

    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;

    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный',
        };
    }
}
?>
```
