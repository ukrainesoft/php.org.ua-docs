---
navigation:
  - reflectionclass.getname.md: '« ReflectionClass::getName'
  - reflectionclass.getparentclass.md: 'ReflectionClass::getParentClass »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getNamespaceName'
---
# ReflectionClass::getNamespaceName

(PHP 5> = 5.3.0, PHP 7, PHP 8)

ReflectionClass::getNamespaceName — Повертає назву простору імен

### Опис

```methodsynopsis
public ReflectionClass::getNamespaceName(): string
```

Повертає назву простору імен.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва простору імен.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getNamespaceName()****

```php
<?php
namespace A\B;

class Foo { }

$class = new \ReflectionClass('stdClass');

var_dump($class->inNamespace());
var_dump($class->getName());
var_dump($class->getNamespaceName());
var_dump($class->getShortName());

$class = new \ReflectionClass('A\\B\\Foo');

var_dump($class->inNamespace());
var_dump($class->getName());
var_dump($class->getNamespaceName());
var_dump($class->getShortName());
?>
```

Результат виконання цього прикладу:

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

-   [ReflectionClass::getParentClass()](reflectionclass.getparentclass.md) - Повертає батьківський клас
-   [namespaces](language.namespaces.md)
