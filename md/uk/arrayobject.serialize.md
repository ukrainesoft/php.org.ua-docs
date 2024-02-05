---
navigation:
  - arrayobject.offsetunset.md: '« ArrayObject::offsetUnset'
  - arrayobject.setflags.md: 'ArrayObject::setFlags »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::serialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::serialize

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

ArrayObject::serialize — Серіалізувати ArrayObject

### Опис

```methodsynopsis
public ArrayObject::serialize(): string
```

Сериализует[ArrayObject](class.arrayobject.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Сериализованное представление[ArrayObject](class.arrayobject.md)

### Приклади

**Пример #1 Пример использования**ArrayObject::serialize()\*\*\*\*

```php
<?php
$o = new ArrayObject();

$s1 = serialize($o);
$s2 = $o->serialize();

var_dump($s1);
var_dump($s2);
?>
```

Результат виконання наведеного прикладу:

```
string(45) "C:11:"ArrayObject":21:{x:i:0;a:0:{};m:a:0:{}}"
string(21) "x:i:0;a:0:{};m:a:0:{}"
```

### Дивіться також

-   [ArrayObject::unserialize()](arrayobject.unserialize.md) \- Десеріалізувати ArrayObject
-   [serialize()](function.serialize.md) \- Генерує придатне для зберігання уявлення змінної
-   [Серіалізація об'єктів](language.oop5.serialization.md)
