Повертає динамічно створене замикання для методу

-   [« ReflectionMethod::export](reflectionmethod.export.html)
    
-   [ReflectionMethod::getDeclaringClass »](reflectionmethod.getdeclaringclass.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionMethod](class.reflectionmethod.html)
    
-   Повертає динамічно створене замикання для методу
    

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