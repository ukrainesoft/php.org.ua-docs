---
navigation:
  - reflectionclass.getmodifiers.md: '« ReflectionClass::getModifiers'
  - reflectionclass.getnamespacename.md: 'ReflectionClass::getNamespaceName »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getName

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getName — Повертає ім'я класу

### Опис

```methodsynopsis
public ReflectionClass::getName(): string
```

Повертає ім'я класу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Назва класу.

### Приклади

**Пример #1 Пример использования**ReflectionClass::getName()\*\*\*\*

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

-   [ReflectionClass::getNamespaceName()](reflectionclass.getnamespacename.md) \- Повертає назву простору імен
