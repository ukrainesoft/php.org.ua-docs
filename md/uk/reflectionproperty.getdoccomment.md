---
navigation:
  - reflectionproperty.getdefaultvalue.md: '« ReflectionProperty::getDefaultValue'
  - reflectionproperty.getmodifiers.md: 'ReflectionProperty::getModifiers »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::getDocComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::getDocComment

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ReflectionProperty::getDocComment — Отримання doc-коментаря для властивості

### Опис

```methodsynopsis
public ReflectionProperty::getDocComment(): string|false
```

Отримує doc-коментар для якості.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Doc-коментар, якщо він існує, інакше **`false`**

### Приклади

**Приклад #1 Приклад**ReflectionProperty::getDocComment()\*\*\*\*

```php
<?php
class Str
{
    /**
     * @var int  Длина строки
     */
    public $length = 5;
}

$prop = new ReflectionProperty('Str', 'length');

var_dump($prop->getDocComment());

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(52) "/**
     * @var int  Длина строки
     */"
```

**Приклад #2 Декларація кількох властивостей**

Якщо doc-коментар заданий перед множинною декларацією, то він вважатиметься таким, що стосується лише першого з них.

```php
<?php
class Foo
{
    /** @var string */
    public $a, $b;
}
$class = new \ReflectionClass('Foo');
foreach ($class->getProperties() as $property) {
    echo $property->getName() . ': ' . var_export($property->getDocComment(), true) . PHP_EOL;
}
?>
```

Результат виконання наведеного прикладу:

```
a: '/** @var string */'
b: false
```

### Дивіться також

-   [ReflectionProperty::getModifiers()](reflectionproperty.getmodifiers.md) \- Отримання модифікаторів властивостей класу
-   [ReflectionProperty::getName()](reflectionproperty.getname.md) \- Отримання імені властивості
-   [ReflectionProperty::getValue()](reflectionproperty.getvalue.md) \- набуває значення
