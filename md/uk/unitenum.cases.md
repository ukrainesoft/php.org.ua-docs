Повертає список варіантів перерахування

-   [« UnitEnum](class.unitenum.md)
    
-   [BackedEnum »](class.backedenum.md)
    
-   [PHP Manual](index.md)
    
-   [UnitEnum](class.unitenum.md)
    
-   Повертає список варіантів перерахування
    

# UnitEnum::cases

(PHP 8> = 8.1.0)

UnitEnum::cases — Повертає список варіантів перерахування

### Опис

```methodsynopsis
public static UnitEnum::cases(): array
```

Метод повертає упакований масив усіх варіантів перерахування у лексичному порядку.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив усіх певних варіантів перерахування у лексичному порядку.

### Приклади

**Приклад #1 Простий приклад використання**

У цьому прикладі показано, як повертаються варіанти перерахування.

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

var_dump(Suit::cases());
?>
```

Результат виконання цього прикладу:

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