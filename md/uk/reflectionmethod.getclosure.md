---
navigation:
  - reflectionmethod.export.html: '« ReflectionMethod::export'
  - reflectionmethod.getdeclaringclass.html: 'ReflectionMethod::getDeclaringClass »'
  - index.html: PHP Manual
  - class.reflectionmethod.html: ReflectionMethod
title: 'ReflectionMethod::getClosure'
---
# ReflectionMethod::getClosure

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionMethod::getClosure — Повертає динамічно створене замикання для методу

### Опис

```methodsynopsis
public ReflectionMethod::getClosure(?object $object = null): Closure
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`object`

Заборонений для статичних методів, є обов'язковим для інших.

### Значення, що повертаються

Повертає замикання [Closure](class.closure.html). Повертає **`null`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `object` тепер допускає значення null. |
