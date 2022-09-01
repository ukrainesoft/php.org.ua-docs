---
navigation:
  - splobjectstorage.getinfo.html: '« SplObjectStorage::getInfo'
  - splobjectstorage.next.html: 'SplObjectStorage::next »'
  - index.html: PHP Manual
  - class.splobjectstorage.html: SplObjectStorage
title: 'SplObjectStorage::key'
---
# SplObjectStorage::key

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання **SplObjectStorage::key()****

```php
<?php
$s = new SplObjectStorage();

$o1 = new StdClass;
$o2 = new StdClass;

$s->attach($o1, "d1");
$s->attach($o2, "d2");

$s->rewind();
while($s->valid()) {
    $index  = $s->key();
    $object = $s->current(); // аналогично current($s)

    var_dump($index);
    var_dump($object);
    $s->next();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(0)
object(stdClass)#2 (0) {
}
int(1)
object(stdClass)#3 (0) {
}
```

### Дивіться також

-   [SplObjectStorage::rewind()](splobjectstorage.rewind.html) - Переводить ітератор на перший елемент контейнера
-   [SplObjectStorage::current()](splobjectstorage.current.html) - Повертає поточний об'єкт
-   [SplObjectStorage::next()](splobjectstorage.next.html) - Перехід до наступного об'єкту
-   [SplObjectStorage::valid()](splobjectstorage.valid.html) - Визначає, чи допустиме поточне значення ітератора
