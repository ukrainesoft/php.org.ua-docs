---
navigation:
  - componere-definition.isregistered.md: '« Componere\\Definition::isRegistered'
  - componere-definition.getclosures.md: 'Componere\\Definition::getClosures »'
  - index.md: PHP Manual
  - class.componere-definition.md: Componere\\Definition
title: 'Componere\\Definition::getClosure'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Definition::getClosure

(Componere 2 >= 2.1.0)

Componere\\Definition::getClosure — Отримує замикання

### Опис

```methodsynopsis
public Componere\Definition::getClosure(string $name): Closure
```

Повинен повернути замикання для вказаного методу

### Список параметрів

`name`

Реєстронезалежне ім'я методу

### Значення, що повертаються

Замикання прив'язане до коректної області

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо `name`не найдено
