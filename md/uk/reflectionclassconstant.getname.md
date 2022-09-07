---
navigation:
  - reflectionclassconstant.getmodifiers.md: '« ReflectionClassConstant::getModifiers'
  - reflectionclassconstant.getvalue.md: 'ReflectionClassConstant::getValue »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::getName'
---
# ReflectionClassConstant::getName

(PHP 7> = 7.1.0, PHP 8)

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

| Версия | Описание |
| --- | --- |
|  | Викидає помилку [Error](class.error.md) якщо властивість name не була ініціалізована. Раніше, у разі помилки, метод повертав **`false`** |
