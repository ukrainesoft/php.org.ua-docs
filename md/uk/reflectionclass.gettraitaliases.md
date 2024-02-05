---
navigation:
  - reflectionclass.getstaticpropertyvalue.md: '« ReflectionClass::getStaticPropertyValue'
  - reflectionclass.gettraitnames.md: 'ReflectionClass::getTraitNames »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getTraitAliases'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getTraitAliases

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionClass::getTraitAliases — Повертає масив псевдонімів трейтів

### Опис

```methodsynopsis
public ReflectionClass::getTraitAliases(): array
```

Отримує масив псевдонімів методів трейтів, визначених у класі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив, ключами якого є нові імена методів, а значеннями – оригінальні імена методів (у форматі `"TraitName::original"`
