---
navigation:
  - reflectionclass.getproperty.md: '« ReflectionClass::getProperty'
  - reflectionclass.getreflectionconstants.md: 'ReflectionClass::getReflectionConstants »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getReflectionConstant'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getReflectionConstant

(PHP 7 >= 7.1.0, PHP 8)

ReflectionClass::getReflectionConstant — Получает[ReflectionClassConstant](class.reflectionclassconstant.md) для константи класу

### Опис

```methodsynopsis
public ReflectionClass::getReflectionConstant(string $name): ReflectionClassConstant|false
```

Отримує [ReflectionClassConstant](class.reflectionclassconstant.md) для якості константи.

### Список параметрів

`name`

Ім'я константи класу.

### Значення, що повертаються

Об'єкт [ReflectionClassConstant](class.reflectionclassconstant.md)или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ReflectionClass::getReflectionConstants()](reflectionclass.getreflectionconstants.md) \- Отримує константи класу
-   [ReflectionClassConstant](class.reflectionclassconstant.md)
