---
navigation:
  - language.enumerations.object-differences.md: « Відмінності від об'єктів
  - language.enumerations.serialization.md: Сериализация »
  - index.md: PHP Manual
  - language.enumerations.md: Перечисления
title: Список значень
---
## Список значень

І чисті перерахування і типізовані перерахування реалізують внутрішній інтерфейс з ім'ям [UnitEnum](class.unitenum.md). . `UnitEnum` включає статичний метод `cases()`. . `cases()` повертає упакований масив усіх певних варіантів у порядку оголошення.

```php
<?php
Suit::cases();
// Produces: [Suit::Hearts, Suit::Diamonds, Suit::Clubs, Suit::Spades]
?>
```

Ручне визначення методу `cases()` у перерахунку призведе до фатальної помилки.
