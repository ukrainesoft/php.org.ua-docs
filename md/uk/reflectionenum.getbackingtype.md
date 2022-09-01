---
navigation:
  - reflectionenum.construct.md: '« ReflectionEnum::construct'
  - reflectionenum.getcase.md: 'ReflectionEnum::getCase »'
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::getBackingType'
---
# ReflectionEnum::getBackingType

(PHP 8> = 8.1.0)

ReflectionEnum::getBackingType — Отримує тип переліку, якщо є

### Опис

```methodsynopsis
public ReflectionEnum::getBackingType(): ?ReflectionType
```

Якщо перелік типизований, цей метод поверне екземпляр [ReflectionType](class.reflectiontype.md) типу перерахування. Якщо це не типізований перелік, метод поверне `null`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [ReflectionType](class.reflectiontype.md) або `null`, якщо перелік не типизований.

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

-   [Перечисления](language.enumerations.md)
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.md) - Визначає, чи є перерахування типовим
