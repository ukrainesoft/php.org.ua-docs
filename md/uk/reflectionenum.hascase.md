---
navigation:
  - reflectionenum.getcases.md: '« ReflectionEnum::getCases'
  - reflectionenum.isbacked.md: 'ReflectionEnum::isBacked »'
  - index.md: PHP Manual
  - class.reflectionenum.md: ReflectionEnum
title: 'ReflectionEnum::hasCase'
---
# ReflectionEnum::hasCase

(PHP 8> = 8.1.0)

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

**Приклад #1 Приклад використання **ReflectionEnum::hasCase()****

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

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```

### Дивіться також

-   [Перечисления](language.enumerations.md)
-   [ReflectionEnum::getCase()](reflectionenum.getcase.md) - Повертає певний варіант перерахування
-   [ReflectionEnum::getCases()](reflectionenum.getcases.md) - Повертає список усіх варіантів перерахування
