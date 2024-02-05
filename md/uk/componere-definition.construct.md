---
navigation:
  - class.componere-definition.md: « Componere\\Definition
  - componere-definition.addconstant.md: 'Componere\\Definition::addConstant »'
  - index.md: PHP Manual
  - class.componere-definition.md: Componere\\Definition
title: 'Componere\\Definition::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Definition::\_\_construct

(Componere 2 >= 2.1.0)

Componere\\Definition::\_\_construct - Визначення конструктора

### Опис

public**Componere\\Definition::\_\_construct**(string`$name`) .

public**Componere\\Definition::\_\_construct**(string`$name`, string`$parent`) .

public**Componere\\Definition::\_\_construct**(string`$name`, array`$interfaces`) .

public**Componere\\Definition::\_\_construct**(string`$name`, string`$parent`, array`$interfaces`) .

### Список параметрів

`name`

Реєстронезалежне ім'я класу

`parent`

Реєстронезалежне ім'я класу

`interfaces`

Масив реєстронезалежних імен класів

### Винятки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо зроблено спробу замінити внутрішній клас

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо зроблено спробу замінити інтерфейс

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md), якщо зроблено спробу замінити трейт

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо клас, зазначений у `interfaces`не найден

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо клас, зазначений у `interfaces` не є інтерфейсом
