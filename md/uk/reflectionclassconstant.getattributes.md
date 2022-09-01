---
navigation:
  - reflectionclassconstant.export.md: '« ReflectionClassConstant::export'
  - reflectionclassconstant.getdeclaringclass.md: 'ReflectionClassConstant::getDeclaringClass »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::getAttributes'
---
# ReflectionClassConstant::getAttributes

(PHP 8)

ReflectionClassConstant::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionClassConstant::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені в цій константі класу у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

### Список параметрів

`name`

`flags`

### Значення, що повертаються

Масив атрибутів як об'єкта [ReflectionAttribute](class.reflectionattribute.md)

### Дивіться також

-   [ReflectionClass::getAttributes()](reflectionclass.getattributes.md) - Отримує атрибути
-   [ReflectionFunctionAbstract::getAttributes()](reflectionfunctionabstract.getattributes.md) - Отримує атрибути
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) - Отримує атрибути
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) - Отримує атрибути
