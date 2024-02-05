---
navigation:
  - serializable.serialize.md: '« Serializable::serialize'
  - class.closure.md: Closure »
  - index.md: PHP Manual
  - class.serializable.md: Serializable
title: 'Serializable::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Serializable::unserialize

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

Serializable::unserialize — Створює об'єкт

### Опис

```methodsynopsis
public Serializable::unserialize(string $data): void
```

Викликається під час десеріалізації об'єкта.

> **Зауваження** :
> 
> Метод діє як [конструктор](language.oop5.decon.md#language.oop5.decon.constructor) об'єкт. Метод [\_\_construct()](language.oop5.decon.md#object.construct) *не* викликається після цього.

### Список параметрів

`data`

Строкове уявлення об'єкта.

### Значення, що повертаються

Значення методу, що повертається, ігнорується.

### Дивіться також

-   [\_\_wakeup()](language.oop5.magic.md#object.wakeup)
-   [\_\_unserialize()](language.oop5.magic.md#object.unserialize)
