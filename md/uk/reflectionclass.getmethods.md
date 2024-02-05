---
navigation:
  - reflectionclass.getmethod.md: '« ReflectionClass::getMethod'
  - reflectionclass.getmodifiers.md: 'ReflectionClass::getModifiers »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getMethods'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getMethods

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getMethods — Повертає список методів у вигляді масиву

### Опис

```methodsynopsis
public ReflectionClass::getMethods(?int $filter = null): array
```

Повертає перелік методів у вигляді масиву.

### Список параметрів

`filter`

Фільтрування результату для включення до списку лише методів із певними атрибутами. За промовчанням фільтрації немає.

Комбінація з наступних констант через логічне АБО: **`ReflectionMethod::IS_STATIC`** **`ReflectionMethod::IS_PUBLIC`** **`ReflectionMethod::IS_PROTECTED`** **`ReflectionMethod::IS_PRIVATE`** **`ReflectionMethod::IS_ABSTRACT`** **`ReflectionMethod::IS_FINAL`**, так що всі методи з *будь-яким* з перерахованих атрибутів буде повернено.

> **Зауваження**: Зверніть увагу, що інші побітові операції, наприклад `~` не працюватимуть так, як очікується. Іншими словами, наприклад, неможливо отримати усі нестатичні методи.

### Значення, що повертаються

Масив (array) об'єктів класу [ReflectionMethod](class.reflectionmethod.md)що відображають кожен метод.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | `filter` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**ReflectionClass::getMethods()\*\*\*\*

```php
<?php
class Apple {
    public function firstMethod() { }
    final protected function secondMethod() { }
    private static function thirdMethod() { }
}

$class = new ReflectionClass('Apple');
$methods = $class->getMethods();
var_dump($methods);
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  object(ReflectionMethod)#2 (2) {
    ["name"]=>
    string(11) "firstMethod"
    ["class"]=>
    string(5) "Apple"
  }
  [1]=>
  object(ReflectionMethod)#3 (2) {
    ["name"]=>
    string(12) "secondMethod"
    ["class"]=>
    string(5) "Apple"
  }
  [2]=>
  object(ReflectionMethod)#4 (2) {
    ["name"]=>
    string(11) "thirdMethod"
    ["class"]=>
    string(5) "Apple"
  }
}
```

**Приклад #2 Приклад фільтрації результату виклику **ReflectionClass::getMethods()****

```php
<?php
class Apple {
    public function firstMethod() { }
    final protected function secondMethod() { }
    private static function thirdMethod() { }
}

$class = new ReflectionClass('Apple');
$methods = $class->getMethods(ReflectionMethod::IS_STATIC | ReflectionMethod::IS_FINAL);
var_dump($methods);
?>
```

Результат виконання наведеного прикладу:

```
array(2) {
  [0]=>
  object(ReflectionMethod)#2 (2) {
    ["name"]=>
    string(12) "secondMethod"
    ["class"]=>
    string(5) "Apple"
  }
  [1]=>
  object(ReflectionMethod)#3 (2) {
    ["name"]=>
    string(11) "thirdMethod"
    ["class"]=>
    string(5) "Apple"
  }
}
```

### Дивіться також

-   [ReflectionClass::getMethod()](reflectionclass.getmethod.md) \- Повертає екземпляр ReflectionMethod для методу класу
-   [get\_class\_methods()](function.get-class-methods.md) \- Повертає масив імен методів класу
