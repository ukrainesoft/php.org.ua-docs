Визначає, чи модуль тимчасовим

-   [« ReflectionExtension::isPersistent](reflectionextension.ispersistent.md)
    
-   [ReflectionExtension::toString »](reflectionextension.tostring.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionExtension](class.reflectionextension.md)
    
-   Визначає, чи модуль тимчасовим
    

# ReflectionExtension::isTemporary

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionExtension::isTemporary — Визначає, чи модуль є тимчасовим

### Опис

```methodsynopsis
public ReflectionExtension::isTemporary(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** для модулів, завантажених функцією [dl()](function.dl.md) **`false`** в іншому випадку.

### Дивіться також

-   [ReflectionExtension::isPersistent()](reflectionextension.ispersistent.md) - Визначає, чи модуль є постійним