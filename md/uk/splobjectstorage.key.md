---
navigation:
  - splobjectstorage.getinfo.md: '« SplObjectStorage::getInfo'
  - splobjectstorage.next.md: 'SplObjectStorage::next »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::key'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::key

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplObjectStorage::key — Повертає індекс поточного положення ітератора

### Опис

```methodsynopsis
public SplObjectStorage::key(): int
```

Повертає індекс поточного становища ітератора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Індекс поточного становища ітератора.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::key()\*\*\*\*

```php
<?php
$s = new SplObjectStorage();

$o1 = new stdClass;
$o2 = new stdClass;

$s->attach($o1, "d1");
$s->attach($o2, "d2");

$s->rewind();
while($s->valid()) {
    $index  = $s->key();
    $object = $s->current(); // аналогично current($s)

    var_dump($index);
    var_dump($object);
    $s->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(0)
object(stdClass)#2 (0) {
}
int(1)
object(stdClass)#3 (0) {
}
```

### Дивіться також

-   [SplObjectStorage::rewind()](splobjectstorage.rewind.md) \- перекладає ітератор на перший елемент контейнера
-   [SplObjectStorage::current()](splobjectstorage.current.md) \- Повертає поточний об'єкт
-   [SplObjectStorage::next()](splobjectstorage.next.md) \- Перехід до наступного об'єкту
-   [SplObjectStorage::valid()](splobjectstorage.valid.md) \- Визначає, чи допустиме поточне значення ітератора
