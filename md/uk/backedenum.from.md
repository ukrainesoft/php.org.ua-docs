Порівнює скаляр з екземпляром перерахування

-   [« BackedEnum](class.backedenum.html)
    
-   [BackedEnum::tryFrom »](backedenum.tryfrom.html)
    
-   [PHP Manual](index.html)
    
-   [BackedEnum](class.backedenum.html)
    
-   Порівнює скаляр з екземпляром перерахування
    

# BackedEnum::from

(PHP 8> = 8.1.0)

BackedEnum::from — Порівняє скаляр з екземпляром перерахування

### Опис

```methodsynopsis
public static BackedEnum::from(int|string $value): static
```

Метод **from()** переводить рядок (string) чи число (int) у відповідне значення перерахування, якщо є. Якщо відповідного значення не визначено, викидається [ValueError](class.valueerror.html)

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
enum Suit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

$h = Suit::from('H');

var_dump($h);

$b = Suit::from('B');
?>
```

Результат виконання цього прикладу:

```
enum(Suit::Hearts)

Fatal error: Uncaught ValueError: "B" is not a valid backing value for enum "Suit" in /file.php:15
```

### Дивіться також

-   [UnitEnum::cases()](unitenum.cases.html) - Повертає список варіантів перерахування
-   [BackedEnum::tryFrom()](backedenum.tryfrom.html) - зіставляє скаляр з екземпляром перерахування або null