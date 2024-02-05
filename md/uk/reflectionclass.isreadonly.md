---
navigation:
  - reflectionclass.isiterateable.md: '« ReflectionClass::isIterateable'
  - reflectionclass.issubclassof.md: 'ReflectionClass::isSubclassOf »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isReadOnly'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isReadOnly

(PHP 8 >= 8.2.0)

ReflectionClass::isReadOnly — Перевіряє, чи клас доступний тільки для читання

### Опис

```methodsynopsis
public ReflectionClass::isReadOnly(): bool
```

Перевіряє, чи є клас [доступним лише для читання](language.oop5.basic.md#language.oop5.basic.class.readonly)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*якщо клас є доступним тільки для читання, в іншому випадку повертає **`false`**

### Приклади

**Пример #1 Пример использования**ReflectionClass::isReadOnly()\*\*\*\*

```php
<?php
class TestClass { }
readonly class TestReadOnlyClass { }

$normalClass = new ReflectionClass('TestClass');
$readonlyClass = new ReflectionClass('TestReadOnlyClass');

var_dump($normalClass->isReadOnly());
var_dump($readonlyClass->isReadOnly());

?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionClass::isAbstract()](reflectionclass.isabstract.md) \- Перевіряє, чи є клас абстрактним
-   [Класи, доступні лише для читання](language.oop5.basic.md#language.oop5.basic.class.readonly)
