---
navigation:
  - arrayobject.offsetexists.md: '« ArrayObject::offsetExists'
  - arrayobject.offsetset.md: 'ArrayObject::offsetSet »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ArrayObject::offsetGet

(PHP 5, PHP 7, PHP 8)

ArrayObject::offsetGet — Повертає значення за вказаним індексом

### Опис

```methodsynopsis
public ArrayObject::offsetGet(mixed $key): mixed
```

### Список параметрів

`key`

Індекс, що посилається на значення.

### Значення, що повертаються

Значение по указанному индексу или\*\*`null`\*\*

### Помилки

Викликає помилку рівня \*\*`E_NOTICE`\*\*якщо зазначений індекс не існує.

### Приклади

**Приклад #1 Приклад використання** ArrayObject::offsetGet()\*\*\*\*

```php
<?php
$arrayobj = new ArrayObject(array('zero', 7, 'example'=>'e.g.'));
var_dump($arrayobj->offsetGet(1));
var_dump($arrayobj->offsetGet('example'));
var_dump($arrayobj->offsetExists('notfound'));
?>
```

Результат виконання наведеного прикладу:

```
int(7)
string(4) "e.g."
bool(false)
```
