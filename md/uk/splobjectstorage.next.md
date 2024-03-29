---
navigation:
  - splobjectstorage.key.md: '« SplObjectStorage::key'
  - splobjectstorage.offsetexists.md: 'SplObjectStorage::offsetExists »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::next'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::next

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplObjectStorage::next — Перехід до наступного об'єкта

### Опис

```methodsynopsis
public SplObjectStorage::next(): void
```

Переміщує ітератор на наступний об'єкт об'єкта в контейнері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::next()\*\*\*\*

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

-   [SPLObjectStorage::rewind()](splobjectstorage.rewind.md) \- перекладає ітератор на перший елемент контейнера
