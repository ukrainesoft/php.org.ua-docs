---
navigation:
  - reflectionproperty.clone.md: '« ReflectionProperty::\_\_clone'
  - reflectionproperty.export.md: 'ReflectionProperty::export »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::\_\_construct

(PHP 5, PHP 7, PHP 8)

ReflectionProperty::\_\_construct - Конструктор класу ReflectionProperty

### Опис

public**ReflectionProperty::\_\_construct**(object|string`$class`, string`$property`) .

### Список параметрів

`class`

Або рядок, що містить ім'я класу, що відображається, або об'єкт.

`property`

Ім'я властивості, яку потрібно відобразити.

### Помилки

Спроба отримати або встановити значення захищеної або закритої властивості призведе до викидання винятку.

### Приклади

**Пример #1 Пример использования**ReflectionProperty::\_\_construct()\*\*\*\*

```php
<?php
class Str
{
    public $length  = 5;
}

// Создание нового объекта класса ReflectionProperty
$prop = new ReflectionProperty('Str', 'length');

// Вывод основной информации об объекте
printf(
    "===> %s%s%s%s свойство '%s' (которое %s)\n" .
    "     имеющее модификаторы %s\n",
        $prop->isPublic() ? ' общедоступное' : '',
        $prop->isPrivate() ? ' закрытое' : '',
        $prop->isProtected() ? ' защищённое' : '',
        $prop->isStatic() ? ' статическое' : '',
        $prop->getName(),
        $prop->isDefault() ? 'объявлено во время компиляции' : 'создано во время выполнения',
        var_export(Reflection::getModifierNames($prop->getModifiers()), 1)
);

// создание экземпляра класса Str
$obj= new Str();

// получение текущего значения
printf("---> Значение: ");
var_dump($prop->getValue($obj));

// Изменение значения
$prop->setValue($obj, 10);
printf("---> Установка значения 10, новое значение: ");
var_dump($prop->getValue($obj));

// Сбросить объект
var_dump($obj);
?>
```

Висновок наведеного прикладу буде схожим на:

```
===> общедоступное свойство 'length' (которое объявлено во время компиляции)
     имеющее модификаторы array (
  0 => 'public',
)
---> Значение: int(5)
---> Установка значения 10, новое значение: int(10)
object(Str)#2 (1) {
  ["length"]=>
  int(10)
}
```

**Приклад #2 Отримання значень захищених та закритих властивостей за допомогою класу [ReflectionProperty](class.reflectionproperty.md)**

```php
<?php

class Foo {
    public $x = 1;
    protected $y = 2;
    private $z = 3;
}

$obj = new Foo;

$prop = new ReflectionProperty('Foo', 'y');
$prop->setAccessible(true);
var_dump($prop->getValue($obj)); // int(2)

$prop = new ReflectionProperty('Foo', 'z');
$prop->setAccessible(true);
var_dump($prop->getValue($obj)); // int(2)

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(2)
int(3)
```

### Дивіться також

-   [ReflectionProperty::getName()](reflectionproperty.getname.md) \- Отримання імені властивості
-   [Конструктори](language.oop5.decon.md#language.oop5.decon.constructor)
