---
navigation:
  - class.componere-patch.md: « ComponerePatch
  - componere-patch.apply.md: 'ComponerePatch::apply »'
  - index.md: PHP Manual
  - class.componere-patch.md: ComponerePatch
title: 'ComponerePatch::construct'
---
# ComponerePatch::construct

(Componere 2 >= 2.1.0)

ComponerePatch::construct - Конструктор класу Patch

### Опис

public **ComponerePatch::construct**(object `$instance`

public **ComponerePatch::construct**(object `$instance`, array `$interfaces`

### Список параметрів

`instance`

Призначення для цього патчу

`interfaces`

Реєстронезалежний масив імен класів

### Винятки

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md)якщо клас не може бути знайдений `interfaces`

**Увага**

Викидає виняток [RuntimeException](class.runtimeexception.md), якщо клас у `interfaces` не є інтерфейсом
