---
navigation:
  - reflectionfunctionabstract.getparameters.md: '« ReflectionFunctionAbstract::getParameters'
  - reflectionfunctionabstract.getshortname.md: 'ReflectionFunctionAbstract::getShortName »'
  - index.md: PHP Manual
  - class.reflectionfunctionabstract.md: ReflectionFunctionAbstract
title: 'ReflectionFunctionAbstract::getReturnType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunctionAbstract::getReturnType

(PHP 7, PHP 8)

ReflectionFunctionAbstract::getReturnType — Отримує оголошений тип значення, що повертається функцією значення

### Опис

```methodsynopsis
public ReflectionFunctionAbstract::getReturnType(): ?ReflectionType
```

Отримує оголошений тип значення, що повертається функцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт класу [ReflectionType](class.reflectiontype.md), якщо у функції оголошено тип значення, що повертається, **`null`** в іншому випадку.

### Приклади

**Пример #1 Пример**ReflectionFunctionAbstract::getReturnType()\*\*\*\*

```php
<?php

function to_int($param) : int {
    return (int) $param;
}

$reflection1 = new ReflectionFunction('to_int');
echo $reflection1->getReturnType();
```

Результат виконання наведеного прикладу:

```
int
```

**Приклад #2 Застосування до вбудованих функцій**

```php
<?php

$reflection2 = new ReflectionFunction('array_merge');

var_dump($reflection2->getReturnType());
```

Результат виконання наведеного прикладу:

```
null
```

Це відбувається через те, що багато внутрішніх функцій не мають оголошених типів для аргументів або значення, що повертається. Тому краще уникати використання цього методу на вбудованих функціях.

### Дивіться також

-   [ReflectionFunctionAbstract::hasReturnType()](reflectionfunctionabstract.hasreturntype.md) \- Перевіряє, чи має функція оголошений тип значення, що повертається
-   [ReflectionType::\_\_toString()](reflectiontype.tostring.md) \- Перетворення на рядок
