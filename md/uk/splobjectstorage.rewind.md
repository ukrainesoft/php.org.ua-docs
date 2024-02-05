---
navigation:
  - splobjectstorage.removeallexcept.md: '« SplObjectStorage::removeAllExcept'
  - splobjectstorage.serialize.md: 'SplObjectStorage::serialize »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::rewind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::rewind

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplObjectStorage::rewind - Перекладає ітератор на перший елемент контейнера

### Опис

```methodsynopsis
public SplObjectStorage::rewind(): void
```

Перекладає ітератор перший елемент контейнера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::rewind()\*\*\*\*

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
    $data   = $s->getInfo();

    var_dump($object);
    var_dump($data);
    $s->next();
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
int(0)
```

### Дивіться також

-   [SplObjectStorage::next()](splobjectstorage.next.md) \- Перехід до наступного об'єкту
