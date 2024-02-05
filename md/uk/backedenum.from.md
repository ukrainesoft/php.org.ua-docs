---
navigation:
  - class.backedenum.md: « BackedEnum
  - backedenum.tryfrom.md: 'BackedEnum::tryFrom »'
  - index.md: PHP Manual
  - class.backedenum.md: BackedEnum
title: 'BackedEnum::from'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# BackedEnum::from

(PHP 8 >= 8.1.0)

BackedEnum::from — Порівняє скаляр з екземпляром перерахування

### Опис

```methodsynopsis
public static BackedEnum::from(int|string $value): static
```

Метод**from()** переводить рядок (string) чи число (int) у відповідне значення перерахування, якщо є. Якщо відповідного значення не визначено, викидається [ValueError](class.valueerror.md)

### Список параметрів

`value`

Скалярне значення для зіставлення з перерахуванням.

### Значення, що повертаються

Випадковий екземпляр цього перерахування.

### Приклади

**Приклад #1 Простий приклад використання**

У цьому прикладі показано, як повертаються варіанти перерахування.

```php
<?php
enum Suit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

$h = Suit::from('H');

var_dump($h);

$b = Suit::from('B');
?>
```

Результат виконання наведеного прикладу:

```
enum(Suit::Hearts)

Fatal error: Uncaught ValueError: "B" is not a valid backing value for enum "Suit" in /file.php:15
```

### Дивіться також

-   [UnitEnum::cases()](unitenum.cases.md) \- Повертає список варіантів перерахування
-   [BackedEnum::tryFrom()](backedenum.tryfrom.md) \- зіставляє скаляр з екземпляром перерахування або null
