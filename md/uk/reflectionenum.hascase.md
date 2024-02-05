---
navigation:
  - reflectionenum.getcases.md: '« ReflectionEnum::getCases'
  - reflectionenum.isbacked.md: 'ReflectionEnum::isBacked »'
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::hasCase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnum::hasCase

(PHP 8 >= 8.1.0)

ReflectionEnum::hasCase — Перевіряє варіант перерахування

### Опис

```methodsynopsis
public ReflectionEnum::hasCase(string $name): bool
```

Повертає, чи визначено цей варіант перерахування.

### Список параметрів

`name`

Варіант переліку для перевірки.

### Значення, що повертаються

Повертає **`true`**, якщо варіант визначений, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования**ReflectionEnum::hasCase()\*\*\*\*

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

var_dump($rEnum->hasCase('Hearts'));
var_dump($rEnum->hasCase('Horseshoes'));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
-   [ReflectionEnum::getCase()](reflectionenum.getcase.md) \- Повертає певний варіант перерахування
-   [ReflectionEnum::getCases()](reflectionenum.getcases.md) \- Повертає список усіх варіантів перерахування
