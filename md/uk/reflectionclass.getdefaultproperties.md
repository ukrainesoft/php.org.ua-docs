---
navigation:
  - reflectionclass.getconstructor.md: '« ReflectionClass::getConstructor'
  - reflectionclass.getdoccomment.md: 'ReflectionClass::getDocComment »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getDefaultProperties'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getDefaultProperties

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getDefaultProperties — Повертає стандартні властивості.

### Опис

```methodsynopsis
public ReflectionClass::getDefaultProperties(): array
```

Повертає властивості класу за умовчанням (включаючи успадковані властивості).

> **Зауваження** :
> 
> Цей метод працює лише статичних властивостей під час використання із внутрішніми класами. Значення за умовчанням статичної властивості не можна відстежувати у класах, визначених користувачем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив (array) властивостей за умовчанням, ключами якого є імена властивостей, а значеннями - відповідні значення за умовчанням або ж **`null`**, якщо цій властивості не було встановлено значення за замовчуванням. Функція не розрізняє статичні та нестатичні властивості, а також не надає інформацію про модифікаторів видимості при виведенні.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getDefaultProperties()\*\*\*\*

```php
<?php
class Bar {
    protected $inheritedProperty = 'унаследованное свойство по умолчанию';
}

class Foo extends Bar {
    public $property = 'свойство по умолчанию';
    private $privateProperty = 'закрытое свойство по умолчанию';
    public static $staticProperty = 'статическое свойство';
    public $defaultlessProperty;
}

$reflectionClass = new ReflectionClass('Foo');
var_dump($reflectionClass->getDefaultProperties());
?>
```

Результат виконання наведеного прикладу:

```
array(5) {
  ["staticProperty"]=>
  string(39) "статическое свойство"
  ["property"]=>
  string(40) "свойство по умолчанию"
  ["privateProperty"]=>
  string(57) "закрытое свойство по умолчанию"
  ["defaultlessProperty"]=>
  NULL
  ["inheritedProperty"]=>
  string(69) "унаследованное свойство по умолчанию"
}
```

### Дивіться також

-   [ReflectionClass::getProperties()](reflectionclass.getproperties.md) \- Повертає властивості
-   [ReflectionClass::getStaticProperties()](reflectionclass.getstaticproperties.md) \- Повертає статичні властивості
-   [ReflectionClass::getProperty()](reflectionclass.getproperty.md) \- Повертає екземпляр ReflectionProperty для якості класу
