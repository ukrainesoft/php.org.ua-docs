---
navigation:
  - language.enumerations.object-differences.md: « Відмінності від об'єктів
  - language.enumerations.serialization.md: Серіалізація »
  - index.md: PHP Manual
  - language.enumerations.md: Перерахування
title: Список значень
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Список значень

І чисті, і типізовані перерахування реалізують внутрішній інтерфейс з ім'ям [UnitEnum](class.unitenum.md). Інтерфейс `UnitEnum` включає статичний метод `cases()`Метод`cases()` повертає упакований масив усіх визначених у перерахуванні варіантів у порядку оголошення.

```php
<?php

Suit::cases();
// Produces: [Suit::Hearts, Suit::Diamonds, Suit::Clubs, Suit::Spades]
?>
```

Ручное определение метода`cases()` у перерахунку призведе до фатальної помилки.
