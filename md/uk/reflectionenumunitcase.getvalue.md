---
navigation:
  - reflectionenumunitcase.getenum.md: '« ReflectionEnumUnitCase::getEnum'
  - class.reflectionenumbackedcase.md: ReflectionEnumBackedCase »
  - index.md: PHP Manual
  - class.reflectionenumunitcase.md: ReflectionEnumUnitCase
title: 'ReflectionEnumUnitCase::getValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionEnumUnitCase::getValue

(PHP 8 >= 8.1.0)

ReflectionEnumUnitCase::getValue — Отримує об'єкт варіанта перерахування, описаний Reflection-об'єктом

### Опис

```methodsynopsis
public ReflectionEnumUnitCase::getValue(): UnitEnum
```

Повертає об'єкт варіанта перерахування, описаний Reflection-об'єктом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт варіанта перерахування описаний Reflection-об'єктом.

### Приклади

**Приклад #1 Приклад використання** ReflectionEnum::getValue()\*\*\*\*

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

$rCase = $rEnum->getCase('Diamonds');

var_dump($rCase->getValue());
?>
```

Результат виконання наведеного прикладу:

```
enum(Suit::Diamonds)
```

### Дивіться також

-   [Перерахування](language.enumerations.md)
