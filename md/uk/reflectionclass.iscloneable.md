---
navigation:
  - reflectionclass.isanonymous.md: '« ReflectionClass::isAnonymous'
  - reflectionclass.isenum.md: 'ReflectionClass::isEnum »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isCloneable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isCloneable

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

ReflectionClass::isCloneable — Перевіряє, чи можна клонувати цей клас

### Опис

```methodsynopsis
public ReflectionClass::isCloneable(): bool
```

Перевіряє, чи можна клонувати цей клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо клас можна клонувати, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::isCloneable()\*\*\*\*

```php
<?php
class NotCloneable {
    public $var1;

    private function __clone() {
    }
}

class Cloneable {
    public $var1;
}

$notCloneable = new ReflectionClass('NotCloneable');
$cloneable = new ReflectionClass('Cloneable');

var_dump($notCloneable->isCloneable());
var_dump($cloneable->isCloneable());
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```
