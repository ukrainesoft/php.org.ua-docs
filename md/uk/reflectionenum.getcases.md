Повертає список усіх варіантів перерахування

-   [« ReflectionEnum::getCase](reflectionenum.getcase.md)
    
-   [ReflectionEnum::hasCase »](reflectionenum.hascase.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionEnum](class.reflectionenum.md)
    
-   Повертає список усіх варіантів перерахування
    

# ReflectionEnum::getCases

(PHP 8> = 8.1.0)

ReflectionEnum::getCases — Повертає список усіх варіантів перерахування

### Опис

```methodsynopsis
public ReflectionEnum::getCases(): array
```

Перелік може містити нуль або більше варіантів. Цей метод отримує всі певні випадки в лексичному порядку (тобто в порядку, в якому вони з'являються у вихідному коді).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив Reflection-об'єктів перерахування, по одному для кожного варіанта перерахування. Для простих перерахувань усі вони будуть екземплярами [ReflectionEnumUnitCase](class.reflectionenumunitcase.md). Для типізованих перерахувань усі вони будуть екземплярами [ReflectionEnumBackedCase](class.reflectionenumbackedcase.md)

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::getCases()****

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

$rEnum = new ReflectionEnum(Suit::class);

$cases = $rEnum->getCases();

foreach ($cases as $rCase) {
    var_dump($rCase->getValue());
}
?>
```

Результат виконання цього прикладу:

```
enum(Suit::Hearts)
enum(Suit::Diamonds)
enum(Suit::Clubs)
enum(Suit::Spades)
```

### Дивіться також

-   [Перечисления](language.enumerations.md)
-   [ReflectionEnum::getCase()](reflectionenum.getcase.md) - Повертає певний варіант перерахування
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.md) - Визначає, чи є перерахування типовим