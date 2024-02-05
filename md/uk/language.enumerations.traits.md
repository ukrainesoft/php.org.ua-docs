---
navigation:
  - language.enumerations.constants.md: « Константи перерахувань
  - language.enumerations.expressions.md: Значення перерахування у постійних виразах »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Трейти
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Трейти

До перерахунків дозволено включати трейти, які будуть поводитися як класи. Застереження полягає в тому, що включаються (`use`) у перерахування трейтах не можна оголошувати властивості. У включеному на перелік трейте можна оголошувати лише способи і статичні способи. Трейт із властивостями призведе до фатальної помилки.

```php
<?php

interface Colorful
{
    public function color(): string;
}

trait Rectangle
{
    public function shape(): string {
        return "Прямоугольник";
    }
}

enum Suit implements Colorful
{
    use Rectangle;

    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;

    public function color(): string
    {
        return match($this) {
            Suit::Hearts, Suit::Diamonds => 'Красный',
            Suit::Clubs, Suit::Spades => 'Чёрный',
        };
    }
}
?>
```
