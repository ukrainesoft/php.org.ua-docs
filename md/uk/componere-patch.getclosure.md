---
navigation:
  - componere-patch.derive.html: '« ComponerePatch::derive'
  - componere-patch.getclosures.html: 'ComponerePatch::getClosures »'
  - index.html: PHP Manual
  - class.componere-patch.html: ComponerePatch
title: 'ComponerePatch::getClosure'
---
# ComponerePatch::getClosure

(Componere 2 >= 2.1.0)

ComponerePatch::getClosure — Отримує замикання

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

Викидає виняток [RuntimeException](class.runtimeexception.html) якщо `name` НЕ знайдений
