---
navigation:
  - reflectionclass.innamespace.md: '« ReflectionClass::inNamespace'
  - reflectionclass.isanonymous.md: 'ReflectionClass::isAnonymous »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isAbstract'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isAbstract

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isAbstract — Перевіряє, чи клас є абстрактним

### Опис

```methodsynopsis
public ReflectionClass::isAbstract(): bool
```

Перевіряє, чи клас абстрактним.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ReflectionClass::isAbstract()\*\*\*\*

```php
<?php
class          TestClass { }
abstract class TestAbstractClass { }

$testClass     = new ReflectionClass('TestClass');
$abstractClass = new ReflectionClass('TestAbstractClass');

var_dump($testClass->isAbstract());
var_dump($abstractClass->isAbstract());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) \- Перевіряє, чи є клас інтерфейсом
-   [Абстрактні класи](language.oop5.abstract.md)
