---
navigation:
  - reflectionproperty.export.md: '« ReflectionProperty::export'
  - reflectionproperty.getdeclaringclass.md: 'ReflectionProperty::getDeclaringClass »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getAttributes'
---
# ReflectionProperty::getAttributes

(PHP 8)

ReflectionProperty::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionProperty::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені в цій властивості класу, у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`name`

`flags`

### Значення, що повертаються

Масив атрибутів як об'єкта [ReflectionAttribute](class.reflectionattribute.md)

### Дивіться також

-   [ReflectionClass::getAttributes()](reflectionclass.getattributes.md) - Отримує атрибути
-   [ReflectionClassConstant::getAttributes()](reflectionclassconstant.getattributes.md) - Отримує атрибути
-   [ReflectionFunctionAbstract::getAttributes()](reflectionfunctionabstract.getattributes.md) - Отримує атрибути
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) - Отримує атрибути
