---
navigation:
  - reflectionparameter.getclass.md: '« ReflectionParameter::getClass'
  - reflectionparameter.getdeclaringfunction.md: 'ReflectionParameter::getDeclaringFunction »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::getDeclaringClass'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionParameter::getDeclaringClass

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

ReflectionParameter::getDeclaringClass — Отримання класу, що оголошує

### Опис

```methodsynopsis
public ReflectionParameter::getDeclaringClass(): ?ReflectionClass
```

Отримує клас, що оголошує.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт класу [ReflectionClass](class.reflectionclass.md), либо\*\*`null`\*\*, якщо викликано для функції.

### Приклади

**Приклад #1 Отримання класу, в якому оголошено метод**

```php
<?php
class Foo
{
    public function bar(\DateTime $datetime)
    {
    }
}

class Baz extends Foo
{
}

$param = new \ReflectionParameter(['Baz', 'bar'], 0);

var_dump($param->getDeclaringClass());
```

Результат виконання наведеного прикладу:

```
object(ReflectionClass)#2 (1) {
  ["name"]=>
  string(3) "Foo"
}
```

### Дивіться також

-   [ReflectionParameter::getClass()](reflectionparameter.getclass.md) \- Отримує об'єкт ReflectionClass для параметра, що відображається, або null
