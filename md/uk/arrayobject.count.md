---
navigation:
  - arrayobject.construct.md: '« ArrayObject::\_\_construct'
  - arrayobject.exchangearray.md: 'ArrayObject::exchangeArray »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::count

(PHP 5, PHP 7, PHP 8)

ArrayObject::count — Отримати кількість загальнодоступних властивостей ArrayObject

### Опис

```methodsynopsis
public ArrayObject::count(): int
```

Отримати кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість загальнодоступних властивостей [ArrayObject](class.arrayobject.md)

> **Зауваження** :
> 
> Якщо [ArrayObject](class.arrayobject.md) створюється з масиву, всі властивості є загальнодоступними.

### Приклади

**Пример #1 Пример использования**ArrayObject::count()\*\*\*\*

```php
<?php
class Example {
    public $public = 'prop:public';
    private $prv   = 'prop:private';
    protected $prt = 'prop:protected';
}

$arrayobj = new ArrayObject(new Example());
var_dump($arrayobj->count());

$arrayobj = new ArrayObject(array('first','second','third'));
var_dump($arrayobj->count());
?>
```

Результат виконання наведеного прикладу:

```
int(1)
int(3)
```
