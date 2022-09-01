---
navigation:
  - language.types.object.md: « Об'єкти
  - language.types.resource.md: Ресурс »
  - index.md: PHP Manual
  - language.types.md: Типи
title: Перерахування
---
## Перерахування

### Основи перерахувань

Перерахування - це обмежує шар над класами і константами класів, призначений надання способу визначення закритого набору можливих значень для типу.

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

function do_stuff(Suit $s)
{
    // ...
}

do_stuff(Suit::Spades);
?>
```

Повний опис дивіться у розділі про [перечислениях](language.enumerations.md)

### Casting

Якщо перерахування (enum) перетворюється на об'єкт (object), воно змінюється. Якщо перерахування (enum) перетворюється на масив (array), масив з одним ключем `name` (для простих перерахувань) або масив з обома ключами `name` і `value` (Для типізованих перерахувань). Решта приведення типів призведе до помилки.
