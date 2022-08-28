Порівнює скаляр з екземпляром перерахування або null

-   [« BackedEnum::from](backedenum.from.html)
    
-   [Контекстные опции и параметры »](context.html)
    
-   [PHP Manual](index.html)
    
-   [BackedEnum](class.backedenum.html)
    
-   Порівнює скаляр з екземпляром перерахування або null
    

# BackedEnum::tryFrom

(PHP 8> = 8.1.0)

BackedEnum::tryFrom — Порівняє скаляр з екземпляром перерахування або null

### Опис

```methodsynopsis
public static BackedEnum::tryFrom(int|string $value): ?static
```

Метод **tryFrom()** переводить рядок (string) чи число (int) у відповідне значення перерахування, якщо є. Якщо значення не визначено, повертається null.

### Список параметрів

`value`

Скалярне значення для зіставлення з перерахуванням.

### Значення, що повертаються

Примірник перерахування або null, якщо екземпляр не знайдено.

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

$h = Suit::tryFrom('H');

var_dump($h);

$b = Suit::tryFrom('B') ?? Suit::Spades;

var_dump($b);
?>
```

Результат виконання цього прикладу:

```
enum(Suit::Hearts)
enum(Suit::Spades)
```

### Дивіться також

-   [UnitEnum::cases()](unitenum.cases.html) - Повертає список варіантів перерахування
-   [BackedEnum::from()](backedenum.from.html) - зіставляє скаляр з екземпляром перерахування