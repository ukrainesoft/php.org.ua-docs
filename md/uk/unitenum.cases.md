---
navigation:
  - class.unitenum.md: « UnitEnum
  - class.backedenum.md: BackedEnum »
  - index.md: PHP Manual
  - class.unitenum.md: UnitEnum
title: 'UnitEnum::cases'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UnitEnum::cases

(PHP 8 >= 8.1.0)

UnitEnum::cases — Повертає список варіантів перерахування

### Опис

```methodsynopsis
public static UnitEnum::cases(): array
```

Метод повертає упакований масив усіх варіантів перерахування у порядку оголошення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив усіх певних варіантів перерахування у порядку оголошення.

### Приклади

**Приклад #1 Простий приклад використання**

У цьому прикладі показано, як повертаються варіанти перерахування.

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

var_dump(Suit::cases());
?>
```

Результат виконання наведеного прикладу:

```
array(4) {
    [0]=>
    enum(Suit::Hearts)
    [1]=>
    enum(Suit::Diamonds)
    [2]=>
    enum(Suit::Clubs)
    [3]=>
    enum(Suit::Spades)
}
```
