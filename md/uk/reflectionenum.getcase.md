---
navigation:
  - reflectionenum.getbackingtype.md: '« ReflectionEnum::getBackingType'
  - reflectionenum.getcases.md: 'ReflectionEnum::getCases »'
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::getCase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnum::getCase

(PHP 8 >= 8.1.0)

ReflectionEnum::getCase — Повертає певний варіант перерахування

### Опис

```methodsynopsis
public ReflectionEnum::getCase(string $name): ReflectionEnumUnitCase
```

Повертає Reflection-об'єкт для певного варіанта перерахування на ім'я. Якщо вибраний варіант не визначено, викидається [ReflectionException](class.reflectionexception.md)

### Список параметрів

`name`

Назву варіанта, який потрібно отримати.

### Значення, що повертаються

Екземпляр [ReflectionEnumUnitCase](class.reflectionenumunitcase.md) або [ReflectionEnumBackedCase](class.reflectionenumbackedcase.md)в зависимости от ситуации.

### Приклади

**Приклад #1 Приклад використання** ReflectionEnum::getCase()\*\*\*\*

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

$rEnum = new ReflectionEnum(Suit::class);

$rCase = $rEnum->getCase('Clubs');

var_dump($rCase->getValue());
?>
```

Результат виконання наведеного прикладу:

```
enum(Suit::Clubs)
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
-   [ReflectionEnum::getCases()](reflectionenum.getcases.md) \- Повертає список усіх варіантів перерахування
-   [ReflectionEnum::hasCase()](reflectionenum.hascase.md) \- Перевіряє варіант перерахування
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.md) \- Визначає, чи є перерахування типовим
