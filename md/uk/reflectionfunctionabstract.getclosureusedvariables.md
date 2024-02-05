---
navigation:
  - reflectionfunctionabstract.getclosurethis.md: '« ReflectionFunctionAbstract::getClosureThis'
  - reflectionfunctionabstract.getdoccomment.md: 'ReflectionFunctionAbstract::getDocComment »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getClosureUsedVariables'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getClosureUsedVariables

(PHP 8 >= 8.1.0)

ReflectionFunctionAbstract::getClosureUsedVariables — Повертає масив змінних, що використовуються в замиканні

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getClosureUsedVariables(): array
```

Повертає масив (array) використовуваних в [Closure](class.closure.md) змінних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) використовуваних в [Closure](class.closure.md) змінних.

### Приклади

**Приклад #1 Приклад використання** ReflectionFunctionAbstract::getClosureUsedVariables()\*\*\*\*

```php
<?php

$one = 1;
$two = 2;

$function = function() use ($one, $two) {
    static $three = 3;
};

$reflector = new ReflectionFunction($function);

var_dump($reflector->getClosureUsedVariables());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(2) {
  ["one"]=>
  int(1)
  ["two"]=>
  int(2)
}
```

### Дивіться також

-   [ReflectionFunctionAbstract::getClosureScopeClass()](reflectionfunctionabstract.getclosurescopeclass.md) \- Повертає клас, в рамках якого було оголошено замикання
-   [ReflectionFunctionAbstract::getClosureThis()](reflectionfunctionabstract.getclosurethis.md) \- Повертає покажчик, прив'язаний до замикання
