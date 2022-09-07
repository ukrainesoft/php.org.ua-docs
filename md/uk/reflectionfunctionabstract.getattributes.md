---
navigation:
  - reflectionfunctionabstract.clone.md: '« ReflectionFunctionAbstract::clone'
  - reflectionfunctionabstract.getclosurescopeclass.md: 'ReflectionFunctionAbstract::getClosureScopeClass »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getAttributes'
---
# ReflectionFunctionAbstract::getAttributes

(PHP 8)

ReflectionFunctionAbstract::getAttributes — Отримує атрибути

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getAttributes(?string $name = null, int $flags = 0): array
```

Повертає всі атрибути, оголошені для цієї функції або методу у вигляді масиву [ReflectionAttribute](class.reflectionattribute.md)

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
-   [ReflectionParameter::getAttributes()](reflectionparameter.getattributes.md) - Отримує атрибути
-   [ReflectionProperty::getAttributes()](reflectionproperty.getattributes.md) - Отримує атрибути
