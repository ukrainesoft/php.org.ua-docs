---
navigation:
  - componere-patch.isapplied.md: '« Componere\\Patch::isApplied'
  - componere-patch.getclosure.md: 'Componere\\Patch::getClosure »'
  - index.md: PHP Manual
  - class.componere-patch.md: Componere\\Patch
title: 'Componere\\Patch::derive'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Patch::derive

(Componere 2 >= 2.1.1)

Componere\\Patch::derive — Отримання патчу

### Опис

```methodsynopsis
public Componere\Patch::derive(object $instance): Patch
```

Повинен отримати Patch для заданого екземпляра `instance`

### Список параметрів

`instance`

Призначення для отриманого патчу

### Значення, що повертаються

Patch для`instance` виходить з поточного Patch

### Винятки

**Увага**

Викидає виняток [InvalidArgumentException](class.invalidargumentexception.md) якщо `instance` не сумісний
