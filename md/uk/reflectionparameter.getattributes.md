---
navigation:
  - reflectionparameter.export.md: '« ReflectionParameter::export'
  - reflectionparameter.getclass.md: 'ReflectionParameter::getClass »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::getAttributes'
---
# ReflectionParameter::getAttributes

(PHP 8)

ReflectionParameter::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionParameter::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені в цьому параметрі у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

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
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) - Отримує атрибути
