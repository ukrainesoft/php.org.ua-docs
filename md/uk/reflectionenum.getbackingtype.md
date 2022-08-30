Отримує тип перерахування, якщо є

-   [« ReflectionEnum::construct](reflectionenum.construct.html)
    
-   [ReflectionEnum::getCase »](reflectionenum.getcase.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionEnum](class.reflectionenum.html)
    
-   Отримує тип перерахування, якщо є
    

# ReflectionEnum::getBackingType

(PHP 8> = 8.1.0)

ReflectionEnum::getBackingType — Отримує тип переліку, якщо є

### Опис

```methodsynopsis
public ReflectionEnum::getBackingType(): ?ReflectionType
```

Якщо перелік типизований, цей метод поверне екземпляр [ReflectionType](class.reflectiontype.html) типу перерахування. Якщо це не типізований перелік, метод поверне `null`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [ReflectionType](class.reflectiontype.html) або `null`, якщо перелік не типизований.

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::getBackingType()****

```php
<?php
enum Suit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

$rEnum = new ReflectionEnum(Suit::class);

$rBackingType = $rEnum->getBackingType();

var_dump((string)$rBackingType);
?>
```

Результат виконання цього прикладу:

```
string(6) "string"
```

### Дивіться також

-   [Перечисления](language.enumerations.html)
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.html) - Визначає, чи є перерахування типовим