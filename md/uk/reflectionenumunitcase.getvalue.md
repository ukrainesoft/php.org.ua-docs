---
navigation:
  - reflectionenumunitcase.getenum.html: '« ReflectionEnumUnitCase::getEnum'
  - class.reflectionenumbackedcase.html: ReflectionEnumBackedCase »
  - index.html: PHP Manual
  - class.reflectionenumunitcase.html: ReflectionEnumUnitCase
title: 'ReflectionEnumUnitCase::getValue'
---
# ReflectionEnumUnitCase::getValue

(PHP 8> = 8.1.0)

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

**Приклад #1 Приклад використання **ReflectionEnum::getValue()****

```php
<?php
enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

$rEnum = new ReflectionEnum(Suit::class);

$rCase = $rEnum->getCase('Diamonds');

var_dump($rCase->getValue());
?>
```

Результат виконання цього прикладу:

```
enum(Suit::Diamonds)
```

### Дивіться також

-   [Перечисления](language.enumerations.html)
