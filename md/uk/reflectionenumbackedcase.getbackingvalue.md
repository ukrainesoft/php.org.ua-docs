---
navigation:
  - reflectionenumbackedcase.construct.md: '« ReflectionEnumBackedCase::construct'
  - class.reflectionzendextension.md: ReflectionZendExtension »
  - index.md: PHP Manual
  - class.reflectionenumbackedcase.md: ReflectionEnumBackedCase
title: 'ReflectionEnumBackedCase::getBackingValue'
---
# ReflectionEnumBackedCase::getBackingValue

(PHP 8> = 8.1.0)

ReflectionEnumBackedCase::getBackingValue — Отримує скалярне значення варіанта перерахування

### Опис

```methodsynopsis
public ReflectionEnumBackedCase::getBackingValue(): int|string
```

Отримує скалярне значення варіанта перерахування.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Скалярне значення варіанта перерахування.

### Приклади

**Приклад #1 Приклад використання **ReflectionEnum::getBackingValue()****

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

$rCase = $rEnum->getCase('Spades');

var_dump($rCase->getBackingValue());
?>
```

Результат виконання цього прикладу:

```
string(1) "S"
```

### Дивіться також

-   [Перечисления](language.enumerations.md)
