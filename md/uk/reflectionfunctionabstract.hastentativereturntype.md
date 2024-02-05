---
navigation:
  - reflectionfunctionabstract.hasreturntype.md: '« ReflectionFunctionAbstract::hasReturnType'
  - reflectionfunctionabstract.innamespace.md: 'ReflectionFunctionAbstract::inNamespace »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::hasTentativeReturnType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::hasTentativeReturnType

(PHP 8 >= 8.1.0)

ReflectionFunctionAbstract::hasTentativeReturnType — Визначає, чи є у функції попередній тип значення, що повертається

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::hasTentativeReturnType(): bool
```

Визначає, чи є у функції попередній тип значення, що повертається.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо у функції є попередній тип значення, що повертається, в іншому випадку повертає **`false`**

### Приклади

**Пример #1 Пример использования**ReflectionFunctionAbstract::hasTentativeReturnType()\*\*\*\*

```php
<?php

$method = new ReflectionMethod(\ArrayAccess::class, 'offsetGet');
var_dump($method->hasTentativeReturnType());
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionFunctionAbstract::getTentativeReturnType()](reflectionfunctionabstract.gettentativereturntype.md) \- Повертає попередній тип значення, що повертається, пов'язаний з функцією
-   [ReflectionFunctionAbstract::hasReturnType()](reflectionfunctionabstract.hasreturntype.md) \- Перевіряє, чи має функція оголошений тип значення, що повертається
-   [Сумісність типів значень, що повертаються, з внутрішніми класами](language.oop5.inheritance.md#language.oop5.inheritance.internal-classes)
