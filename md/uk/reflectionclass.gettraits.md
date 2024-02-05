---
navigation:
  - reflectionclass.gettraitnames.md: '« ReflectionClass::getTraitNames'
  - reflectionclass.hasconstant.md: 'ReflectionClass::hasConstant »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getTraits'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getTraits

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionClass::getTraits — Повертає масив трейтів, що використовуються у цьому класі

### Опис

```methodsynopsis
public ReflectionClass::getTraits(): array
```

Отримує масив трейтів, що використовуються у цьому класі

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив, ключами якого є імена трейтів, а значеннями – об'єкти [ReflectionClass](class.reflectionclass.md) для кожного трейта. У разі виникнення помилки повертає **`null`**
