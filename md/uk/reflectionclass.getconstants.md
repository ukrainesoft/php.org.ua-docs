---
navigation:
  - reflectionclass.getconstant.md: '« ReflectionClass::getConstant'
  - reflectionclass.getconstructor.md: 'ReflectionClass::getConstructor »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getConstants'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getConstants

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getConstants — Повертає константи

### Опис

```methodsynopsis
public ReflectionClass::getConstants(?int $filter = null): array
```

Повертає всі визначені класі константи, незалежно від своїх модифікаторів видимості.

### Список параметрів

`filter`

Додатковий фільтр для фільтрації констант видимості. Він налаштовується за допомогою [ReflectionClassConstant constants](class.reflectionclassconstant.md#reflectionclassconstant.constants.modifiers) і за умовчанням використовується всім констант видимості.

### Значення, що повертаються

Масив (array) констант. Ім'я константи – ключ, значення константи – значення.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Добавлен параметр`filter` |

### Дивіться також

-   [ReflectionClass::getConstant()](reflectionclass.getconstant.md) \- Повертає певну константу
