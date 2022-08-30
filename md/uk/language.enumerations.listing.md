Список значень

-   [« Відмінності від об'єктів](language.enumerations.object-differences.html)
    
-   [Сериализация »](language.enumerations.serialization.md)
    
-   [PHP Manual](index.md)
    
-   [Перечисления](language.enumerations.md)
    
-   Список значень
    

## Список значень

І чисті перерахування і типізовані перерахування реалізують внутрішній інтерфейс з ім'ям [UnitEnum](class.unitenum.md). . `UnitEnum` включає статичний метод `cases()`. . `cases()` повертає упакований масив усіх певних варіантів у порядку оголошення.

```php
<?php
Suit::cases();
// Produces: [Suit::Hearts, Suit::Diamonds, Suit::Clubs, Suit::Spades]
?>
```

Ручне визначення методу `cases()` у перерахунку призведе до фатальної помилки.