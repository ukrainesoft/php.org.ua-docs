---
navigation:
  - arrayobject.offsetunset.html: '« ArrayObject::offsetUnset'
  - arrayobject.setflags.html: 'ArrayObject::setFlags »'
  - index.html: PHP Manual
  - class.arrayobject.html: ArrayObject
title: 'ArrayObject::serialize'
---
# ArrayObject::serialize

(PHP 5> = 5.3.0, PHP 7, PHP 8)

ArrayObject::serialize — Серіалізувати ArrayObject

### Опис

```methodsynopsis
public ArrayObject::serialize(): string
```

Серіалізує [ArrayObject](class.arrayobject.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Серіалізоване подання [ArrayObject](class.arrayobject.html)

### Приклади

**Приклад #1 Приклад використання **ArrayObject::serialize()****

```php
<?php
$o = new ArrayObject();

$s1 = serialize($o);
$s2 = $o->serialize();

var_dump($s1);
var_dump($s2);
?>
```

Результат виконання цього прикладу:

```
string(45) "C:11:"ArrayObject":21:{x:i:0;a:0:{};m:a:0:{}}"
string(21) "x:i:0;a:0:{};m:a:0:{}"
```

### Дивіться також

-   [ArrayObject::unserialize()](arrayobject.unserialize.html) - Десеріалізувати ArrayObject
-   [serialize()](function.serialize.html) - Генерує придатне для зберігання подання змінної
-   [Серіалізація об'єктів](language.oop5.serialization.html)
