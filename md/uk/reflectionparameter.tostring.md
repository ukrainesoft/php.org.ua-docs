---
navigation:
  - reflectionparameter.isvariadic.md: '« ReflectionParameter::isVariadic'
  - class.reflectionproperty.md: ReflectionProperty »
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::\_\_function toString() { \[native code\] }'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::\_\_function toString() { \[native code\] }

(PHP 5, PHP 7, PHP 8)

ReflectionParameter::\_\_toString — Перетворення на рядок

### Опис

```methodsynopsis
public ReflectionParameter::__toString(): string
```

Отримує строкове представлення параметра.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає строкове представлення параметра.

### Приклади

**Приклад #1 Приклад використання** ReflectionParameter::\_\_toString()\*\*\*\*

```php
<?php
echo new ReflectionParameter('substr', 0);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Parameter #0 [ <required> string $string ]
```

### Дивіться також

-   [ReflectionFunction::\_\_toString()](reflectionfunction.tostring.md) \- Повертає рядкову виставу об'єкта ReflectionFunction
-   [ReflectionMethod::\_\_toString()](reflectionmethod.tostring.md) \- Повертає рядкову виставу об'єкта ReflectionMethod
-   [\_\_toString()](language.oop5.magic.md#object.tostring)
