---
navigation:
  - reflectionclass.isenum.md: '« ReflectionClass::isEnum'
  - reflectionclass.isinstance.md: 'ReflectionClass::isInstance »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isFinal'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isFinal

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isFinal — Перевіряє, чи є клас остаточним (final)

### Опис

```methodsynopsis
public ReflectionClass::isFinal(): bool
```

Перевіряє, чи клас остаточним (final).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::isFinal()\*\*\*\*

```php
<?php
class       TestClass { }
final class TestFinalClass { }

$normalClass = new ReflectionClass('TestClass');
$finalClass  = new ReflectionClass('TestFinalClass');

var_dump($normalClass->isFinal());
var_dump($finalClass->isFinal());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isAbstract()](reflectionclass.isabstract.md) \- Перевіряє, чи є клас абстрактним
-   [Ключове слово "final"](language.oop5.final.md)
