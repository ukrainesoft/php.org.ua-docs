---
navigation:
  - reflectionenum.hascase.md: '« ReflectionEnum::hasCase'
  - class.reflectionenumunitcase.md: ReflectionEnumUnitCase »
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::isBacked'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnum::isBacked

(PHP 8 >= 8.1.0)

ReflectionEnum::isBacked — Визначає, чи перелік типизований

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

**Пример #1 Пример использования**ReflectionEnum::isBacked()\*\*\*\*

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

enum BackedSuit: string
{
    case Hearts = 'H';
    case Diamonds = 'D';
    case Clubs = 'C';
    case Spades = 'S';
}

var_dump((new ReflectionEnum(Suit::class))->isBacked());
var_dump((new ReflectionEnum(BackedSuit::class))->isBacked());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
-   [ReflectionEnum::getBackingType()](reflectionenum.getbackingtype.md) \- Отримує тип перерахування, якщо є
