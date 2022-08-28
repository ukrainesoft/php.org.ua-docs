Повертає певний варіант перерахування

-   [« ReflectionEnum::getBackingType](reflectionenum.getbackingtype.html)
    
-   [ReflectionEnum::getCases »](reflectionenum.getcases.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionEnum](class.reflectionenum.html)
    
-   Повертає певний варіант перерахування
    

# ReflectionEnum::getCase

(PHP 8> = 8.1.0)

ReflectionEnum::getCase — Повертає певний варіант перерахування

### Опис

```methodsynopsis
public ReflectionEnum::getCase(string $name): ReflectionEnumUnitCase
```

Повертає Reflection-об'єкт для певного варіанта перерахування на ім'я. Якщо вибраний варіант не визначено, викидається [ReflectionException](class.reflectionexception.html)

### Список параметрів

`name`

Назву варіанта, який потрібно отримати.

### Значення, що повертаються

Екземпляр [ReflectionEnumUnitCase](class.reflectionenumunitcase.html) або [ReflectionEnumBackedCase](class.reflectionenumbackedcase.html) в залежності від ситуації.

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::getCase()****

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

$rCase = $rEnum->getCase('Clubs');

var_dump($rCase->getValue());
?>
```

Результат виконання цього прикладу:

```
enum(Suit::Clubs)
```

### Дивіться також

-   [Перечисления](language.enumerations.html)
-   [ReflectionEnum::getCases()](reflectionenum.getcases.html) - Повертає список усіх варіантів перерахування
-   [ReflectionEnum::hasCase()](reflectionenum.hascase.html) - Перевіряє варіант перерахування
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.html) - Визначає, чи є перерахування типовим