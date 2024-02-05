---
navigation:
  - splfixedarray.setsize.md: '« SplFixedArray::setSize'
  - splfixedarray.unserialize.md: 'SplFixedArray::\_\_unserialize »'
  - index.md: PHP Manual
  - class.splfixedarray.md: SplFixedArray
title: 'SplFixedArray::toArray'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplFixedArray::toArray

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplFixedArray::toArray — Повертає звичайний PHP-масив зі значеннями фіксованого масиву

### Опис

```methodsynopsis
public SplFixedArray::toArray(): array
```

Повертає стандартний PHP-масив зі значеннями фіксованого масиву.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає PHP-масив (array), складений із значень фіксованого масиву.

### Приклади

**Пример #1 Пример использования**SplFixedArray::toArray()\*\*\*\*

```php
<?php
$fa = new SplFixedArray(3);
$fa[0] = 0;
$fa[2] = 2;
var_dump($fa->toArray());
?>
```

Результат виконання наведеного прикладу:

```
array(3) {
  [0]=>
  int(0)
  [1]=>
  NULL
  [2]=>
  int(2)
}
```
