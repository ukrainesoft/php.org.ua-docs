---
navigation:
  - reflectionenumbackedcase.construct.md: '« ReflectionEnumBackedCase::\_\_construct'
  - class.reflectionzendextension.md: ReflectionZendExtension »
  - index.md: PHP Manual
  - class.reflectionenumbackedcase.md: ReflectionEnumBackedCase
title: 'ReflectionEnumBackedCase::getBackingValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnumBackedCase::getBackingValue

(PHP 8 >= 8.1.0)

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

**Приклад #1 Приклад використання** ReflectionEnum::getBackingValue()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
string(1) "S"
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
