---
navigation:
  - reflectionclass.getstaticpropertyvalue.md: '« ReflectionClass::getStaticPropertyValue'
  - reflectionclass.gettraitnames.md: 'ReflectionClass::getTraitNames »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getTraitAliases'
---
# ReflectionClass::getTraitAliases

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionClass::getTraitAliases — Повертає масив псевдонімів трейтів

### Опис

```methodsynopsis
public ReflectionClass::getTraitAliases(): array
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив, ключами якого є нові імена методів, а значеннями - оригінальні імена методів (у форматі `"TraitName::original"`). У разі виникнення помилки повертає **`null`**
