---
navigation:
  - reflectionclass.implementsinterface.md: '« ReflectionClass::implementsInterface'
  - reflectionclass.isabstract.md: 'ReflectionClass::isAbstract »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::inNamespace'
---
# ReflectionClass::inNamespace

(PHP 5> = 5.3.0, PHP 7, PHP 8)

ReflectionClass::inNamespace — Перевіряє, чи визначений клас у просторі імен

### Опис

```methodsynopsis
public ReflectionClass::inNamespace(): bool
```

Перевіряє, чи клас у просторі імен.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::inNamespace()****

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

-   [ReflectionClass::getNamespaceName()](reflectionclass.getnamespacename.md) - Повертає назву простору імен
-   [Пространства имён PHP](language.namespaces.md)
