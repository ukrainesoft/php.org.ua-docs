---
navigation:
  - componere-definition.getclosure.md: '« Componere\\Definition::getClosure'
  - class.componere-patch.md: Componere\\Patch »
  - index.md: PHP Manual
  - class.componere-definition.md: Componere\\Definition
title: 'Componere\\Definition::getClosures'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Definition::getClosures

(Componere 2 >= 2.1.0)

Componere\\Definition::getClosures — Отримує замикання

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
