---
navigation:
  - class.componere-patch.md: « Componere\\Patch
  - componere-patch.apply.md: 'Componere\\Patch::apply »'
  - index.md: PHP Manual
  - class.componere-patch.md: Componere\\Patch
title: 'Componere\\Patch::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Componere\\Patch::\_\_construct

(Componere 2 >= 2.1.0)

Componere\\Patch::\_\_construct - Конструктор класу Patch

### Опис

public**Componere\\Patch::\_\_construct**(object`$instance`) .

public**Componere\\Patch::\_\_construct**(object`$instance`, array`$interfaces`) .

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
