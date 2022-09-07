---
navigation:
  - reflectionclass.getproperty.md: '« ReflectionClass::getProperty'
  - reflectionclass.getreflectionconstants.md: 'ReflectionClass::getReflectionConstants »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getReflectionConstant'
---
# ReflectionClass::getReflectionConstant

(PHP 7> = 7.1.0, PHP 8)

ReflectionClass::getReflectionConstant — Отримує [ReflectionClassConstant](class.reflectionclassconstant.md) для константи класу

### Опис

```methodsynopsis
public ReflectionClass::getReflectionConstant(string $name): ReflectionClassConstant|false
```

Отримує [ReflectionClassConstant](class.reflectionclassconstant.md) для якості константи.

### Список параметрів

`name`

Назва константи класу.

### Значення, що повертаються

Об'єкт [ReflectionClassConstant](class.reflectionclassconstant.md) або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ReflectionClass::getReflectionConstants()](reflectionclass.getreflectionconstants.md) - Отримує константи класу
-   [ReflectionClassConstant](class.reflectionclassconstant.md)
