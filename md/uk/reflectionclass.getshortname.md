---
navigation:
  - reflectionclass.getreflectionconstants.md: '« ReflectionClass::getReflectionConstants'
  - reflectionclass.getstartline.md: 'ReflectionClass::getStartLine »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getShortName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getShortName

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

ReflectionClass::getShortName — Повертає коротке ім'я

### Опис

```methodsynopsis
public ReflectionClass::getShortName(): string
```

Повертає коротке ім'я класу, частина, яка не належить до назви простору імен.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Коротка назва класу.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getShortName()\*\*\*\*

```php
<?php
namespace A\B;

class Foo { }

$function = new \ReflectionClass('stdClass');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());

$function = new \ReflectionClass('A\\B\\Foo');

var_dump($function->inNamespace());
var_dump($function->getName());
var_dump($function->getNamespaceName());
var_dump($function->getShortName());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
string(8) "stdClass"
string(0) ""
string(8) "stdClass"

bool(true)
string(7) "A\B\Foo"
string(3) "A\B"
string(3) "Foo"
```

### Дивіться також

-   [ReflectionClass::getName()](reflectionclass.getname.md) \- Повертає ім'я класу
