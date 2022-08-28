Визначає, чи є перелік типовим

-   [« ReflectionEnum::hasCase](reflectionenum.hascase.html)
    
-   [ReflectionEnumUnitCase »](class.reflectionenumunitcase.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionEnum](class.reflectionenum.html)
    
-   Визначає, чи є перелік типовим
    

# ReflectionEnum::isBacked

(PHP 8> = 8.1.0)

ReflectionEnum::isBacked — Визначає, чи є перелік типовим

### Опис

```methodsynopsis
public ReflectionEnum::isBacked(): bool
```

Типізоване перерахування має власний скалярний еквівалент, або рядок (string), або ціле число (int). Не всі переліки є типізованими.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо перерахування є типізованим, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::isBacked()****

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

enum BackedSuit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

var_dump((new ReflectionEnum(Suit::class))->isBacked());
var_dump((new ReflectionEnum(BackedSuit::class))->isBacked());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [Перечисления](language.enumerations.html)
-   [ReflectionEnum::getBackingType()](reflectionenum.getbackingtype.html) - Отримує тип перерахування, якщо є