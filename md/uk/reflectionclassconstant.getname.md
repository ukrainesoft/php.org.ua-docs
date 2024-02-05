---
navigation:
  - reflectionclassconstant.getmodifiers.md: '« ReflectionClassConstant::getModifiers'
  - reflectionclassconstant.getvalue.md: 'ReflectionClassConstant::getValue »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClassConstant::getName

(PHP 7 >= 7.1.0, PHP 8)

ReflectionClassConstant::getName — Отримати ім'я константи

### Опис

```methodsynopsis
public ReflectionClassConstant::getName(): string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я константи.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Викидає помилку [Error](class.error.md) якщо властивість name не була ініціалізована. Раніше, у разі помилки, метод повертав **`false`** |
