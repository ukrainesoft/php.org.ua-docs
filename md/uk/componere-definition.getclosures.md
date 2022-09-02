---
navigation:
  - componere-definition.getclosure.md: '« ComponereDefinition::getClosure'
  - class.componere-patch.md: ComponerePatch »
  - index.md: PHP Manual
  - class.componere-definition.md: ComponereDefinition
title: 'ComponereDefinition::getClosures'
---
# ComponereDefinition::getClosures

(Componere 2 >= 2.1.0)

ComponereDefinition::getClosures — Отримує замикання

### Опис

```methodsynopsis
public Componere\Definition::getClosures(): array
```

Повертає масив замикань

### Значення, що повертаються

Повертає всі методи у вигляді масиву об'єктів Closure, прив'язаних до коректної області

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо Definition вже було зареєстровано
