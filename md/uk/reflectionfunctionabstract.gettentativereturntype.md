---
navigation:
  - reflectionfunctionabstract.getstaticvariables.html: '« ReflectionFunctionAbstract::getStaticVariables'
  - reflectionfunctionabstract.hasreturntype.html: 'ReflectionFunctionAbstract::hasReturnType »'
  - index.html: PHP Manual
  - class.reflectionfunctionabstract.html: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getTentativeReturnType'
---
# ReflectionFunctionAbstract::getTentativeReturnType

(PHP 8> = 8.1.0)

ReflectionFunctionAbstract::getTentativeReturnType — Повертає попередній тип значення, що повертається, пов'язаний з функцією

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getTentativeReturnType(): ?ReflectionType
```

Повертає попередній тип значення, що повертається, пов'язаний з функцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [ReflectionType](class.reflectiontype.html), якщо вказано попередній тип значення, що повертається, в іншому випадку повертає **`null`**

### Приклади

**Приклад #1 Приклад використання **ReflectionFunctionAbstract::getTentativeReturnType()****

```php
<?php

$method = new ReflectionMethod(\ArrayAccess::class, 'offsetGet');
var_dump($method->getTentativeReturnType());
```

Результатом виконання цього прикладу буде щось подібне:

```
object(ReflectionNamedType)#2 (0) {
}
```

### Дивіться також

-   [ReflectionFunctionAbstract::getReturnType()](reflectionfunctionabstract.getreturntype.html) - Отримує оголошений тип значення, що повертається функцією значення
-   [ReflectionFunctionAbstract::hasTentativeReturnType()](reflectionfunctionabstract.hastentativereturntype.html) - Визначає, чи є у функції попередній тип значення, що повертається
-   [Сумісність типів значень, що повертаються, з внутрішніми класами](language.oop5.inheritance.html#language.oop5.inheritance.internal-classes)
