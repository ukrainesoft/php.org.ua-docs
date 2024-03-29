---
navigation:
  - reflectionclass.getreflectionconstant.md: '« ReflectionClass::getReflectionConstant'
  - reflectionclass.getshortname.md: 'ReflectionClass::getShortName »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getReflectionConstants'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getReflectionConstants

(PHP 7 >= 7.1.0, PHP 8)

ReflectionClass::getReflectionConstants — Отримує константи класу

### Опис

```methodsynopsis
public ReflectionClass::getReflectionConstants(?int $filter = null): array
```

Отримує reflected (відбиті) константи.

### Список параметрів

`filter`

Додатковий фільтр для фільтрації констант видимості. Він налаштовується за допомогою [ReflectionClassConstant constants](class.reflectionclassconstant.md#reflectionclassconstant.constants.modifiers) і за умовчанням використовується всім констант видимості.

### Значення, що повертаються

Масив об'єктів [ReflectionClassConstant](class.reflectionclassconstant.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Добавлен параметр`filter` |

### Приклади

**Приклад #1 Простий приклад використання **ReflectionClass::getReflectionConstants()****

```php
<?php
class Foo {
    public    const FOO  = 1;
    protected const BAR  = 2;
    private   const BAZ  = 3;
}

$foo = new Foo();

$reflect = new ReflectionClass($foo);
$consts  = $reflect->getReflectionConstants();

foreach ($consts as $const) {
    print $const->getName() . "\n";
}

var_dump($consts);

?>
```

Висновок наведеного прикладу буде схожим на:

```
FOO
BAR
BAZ
array(3) {
  [0]=>
  object(ReflectionClassConstant)#3 (2) {
    ["name"]=>
    string(3) "FOO"
    ["class"]=>
    string(3) "Foo"
  }
  [1]=>
  object(ReflectionClassConstant)#4 (2) {
    ["name"]=>
    string(3) "BAR"
    ["class"]=>
    string(3) "Foo"
  }
  [2]=>
  object(ReflectionClassConstant)#5 (2) {
    ["name"]=>
    string(3) "BAZ"
    ["class"]=>
    string(3) "Foo"
  }
}
```

### Дивіться також

-   [ReflectionClass::getReflectionConstant()](reflectionclass.getreflectionconstant.md) \- Отримує ReflectionClassConstant для константи класу
-   [ReflectionClassConstant](class.reflectionclassconstant.md)
