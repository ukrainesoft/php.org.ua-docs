---
navigation:
  - reflectionenum.construct.md: '« ReflectionEnum::\_\_construct'
  - reflectionenum.getcase.md: 'ReflectionEnum::getCase »'
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::getBackingType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnum::getBackingType

(PHP 8 >= 8.1.0)

ReflectionEnum::getBackingType — Отримує тип переліку, якщо є

### Опис

```methodsynopsis
public ReflectionEnum::getBackingType(): ?ReflectionNamedType
```

Якщо перелік типизований, цей метод поверне екземпляр [ReflectionType](class.reflectiontype.md) типу перерахування. Якщо це не типізований перелік, метод поверне `null`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр [ReflectionNamedType](class.reflectionnamedtype.md)или`null`, якщо перелік не типизований.

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер `?ReflectionNamedType`; раніше тип значення, що повертався `?ReflectionType` |

### Приклади

**Приклад #1 Приклад використання** ReflectionEnum::getBackingType()\*\*\*\*

```php
<?php
enum Suit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

$rEnum = new ReflectionEnum(Suit::class);

$rBackingType = $rEnum->getBackingType();

var_dump((string)$rBackingType);
?>
```

Результат виконання наведеного прикладу:

```
string(6) "string"
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
-   [ReflectionEnum::isBacked()](reflectionenum.isbacked.md) \- Визначає, чи є перерахування типовим
