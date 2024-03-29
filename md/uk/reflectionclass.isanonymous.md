---
navigation:
  - reflectionclass.isabstract.md: '« ReflectionClass::isAbstract'
  - reflectionclass.iscloneable.md: 'ReflectionClass::isCloneable »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isAnonymous'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isAnonymous

(PHP 7, PHP 8)

ReflectionClass::isAnonymous — Перевіряє, чи є клас анонімним

### Опис

```methodsynopsis
public ReflectionClass::isAnonymous(): bool
```

Перевіряє, чи анонімний клас ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад**ReflectionClass::isAnonymous()\*\*\*\*

```php
<?php
class TestClass {}
$anonClass = new class {};

$normalClass = new ReflectionClass('TestClass');
$anonClass  = new ReflectionClass($anonClass);

var_dump($normalClass->isAnonymous());
var_dump($anonClass->isAnonymous());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isFinal()](reflectionclass.isfinal.md) \- Перевіряє, чи є клас остаточним (final)
