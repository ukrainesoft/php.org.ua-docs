---
navigation:
  - componere-patch.derive.md: '« Componere\\Patch::derive'
  - componere-patch.getclosures.md: 'Componere\\Patch::getClosures »'
  - index.md: PHP Manual
  - class.componere-patch.md: Componere\\Patch
title: 'Componere\\Patch::getClosure'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Patch::getClosure

(Componere 2 >= 2.1.0)

Componere\\Patch::getClosure — Отримує замикання

### Опис

```methodsynopsis
public Componere\Patch::getClosure(string $name): Closure
```

Повинен повернути замикання для вказаного методу

### Список параметрів

`name`

Реєстронезалежне ім'я методу

### Значення, що повертаються

Замикання, прив'язане до правильної області та об'єкту

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md) якщо `name`не найден
