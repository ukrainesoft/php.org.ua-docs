---
navigation:
  - splobjectstorage.unserialize.md: '« SplObjectStorage::unserialize'
  - spl.iterators.md: Ітератори »
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::valid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::valid

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplObjectStorage::valid — Визначає, чи допустиме поточне значення ітератора

### Опис

```methodsynopsis
public SplObjectStorage::valid(): bool
```

Визначає, чи допустиме поточне значення ітератора, тобто чи можлива робота з цим об'єктом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо поточний об'єкт допустимо і **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::valid()\*\*\*\*

```php
<?php
$s = new SplObjectStorage();

$o1 = new stdClass;
$o2 = new stdClass;

$s->attach($o1, "d1");
$s->attach($o2, "d2");

$s->rewind();
while($s->valid()) {
    echo $s->key()."\n";
    $s->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
0
1
```

### Дивіться також

-   [SplObjectStorage::current()](splobjectstorage.current.md) \- Повертає поточний об'єкт
-   [SplObjectStorage::getInfo()](splobjectstorage.getinfo.md) \- Повертає дані, що асоціюються з поточним об'єктом
