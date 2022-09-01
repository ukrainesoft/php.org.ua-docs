---
navigation:
  - arrayobject.offsetexists.md: '« ArrayObject::offsetExists'
  - arrayobject.offsetset.md: 'ArrayObject::offsetSet »'
  - index.md: PHP Manual
  - class.arrayobject.md: ArrayObject
title: 'ArrayObject::offsetGet'
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

Значення за вказаним індексом або **`null`**

### Помилки

Викликає помилку рівня \*\*`E_NOTICE`\*\*якщо зазначений індекс не існує.

### Приклади

**Приклад #1 Приклад використання **ArrayObject::offsetGet()****

```php
<?php
$arrayobj = new ArrayObject(array('zero', 7, 'example'=>'e.g.'));
var_dump($arrayobj->offsetGet(1));
var_dump($arrayobj->offsetGet('example'));
var_dump($arrayobj->offsetExists('notfound'));
?>
```

Результат виконання цього прикладу:

```
int(7)
string(4) "e.g."
bool(false)
```
