---
navigation:
  - reflectionclass.getdefaultproperties.md: '« ReflectionClass::getDefaultProperties'
  - reflectionclass.getendline.md: 'ReflectionClass::getEndLine »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getDocComment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getDocComment

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getDocComment — Повертає doc-блоки коментарів

### Опис

```methodsynopsis
public ReflectionClass::getDocComment(): string|false
```

Отримує doc-блоки із коментарів класу. Doc-блок - це коментар, що починається з `/**`, За яким слідує пробіл. Якщо над декларацією класу є кілька doc-блоків, то буде повернено найближчий до декларації.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

doc-блок коментарів, якщо він існує, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getDocComment()\*\*\*\*

```php
<?php
/**
* Тестовый класс
*
* @param  foo bar
* @return baz
*/
class TestClass { }

$rc = new ReflectionClass('TestClass');
var_dump($rc->getDocComment());
?>
```

Результат виконання наведеного прикладу:

```
string(55) "/**
* Тестовый класс
*
* @param  foo bar
* @return baz
*/"
```

### Дивіться також

-   [ReflectionClass::getName()](reflectionclass.getname.md) \- Повертає ім'я класу
