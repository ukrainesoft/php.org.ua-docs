---
navigation:
  - splobjectstorage.count.md: '« SplObjectStorage::count'
  - splobjectstorage.detach.md: 'SplObjectStorage::detach »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::current'
---
# SplObjectStorage::current

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObjectStorage::current — Повертає поточний об'єкт

### Опис

```methodsynopsis
public SplObjectStorage::current(): object
```

Повертає поточний об'єкт.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт (object) який вказує ітератор контейнера.

### список змін

| Версия | Описание |
| --- | --- |
|  | Метод **SplObjectStorage::current()** тепер викидає виняток [Error](class.error.md), якщо поточна позиція є неприпустимою. Раніше натомість поверталося значення **`false`** |

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::current()****

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
    $data   = $s->getInfo();

    var_dump($object);
    var_dump($data);
    $s->next();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#2 (0) {
}
string(2) "d1"
object(stdClass)#3 (0) {
}
string(2) "d2"
```

### Дивіться також

-   [SplObjectStorage::rewind()](splobjectstorage.rewind.md) - перекладає ітератор на перший елемент контейнера
-   [SplObjectStorage::key()](splobjectstorage.key.md) - Повертає індекс поточного становища ітератора
-   [SplObjectStorage::next()](splobjectstorage.next.md) - Перехід до наступного об'єкту
-   [SplObjectStorage::valid()](splobjectstorage.valid.md) - Визначає, чи допустиме поточне значення ітератора
-   [SplObjectStorage::getInfo()](splobjectstorage.getinfo.md) - Повертає дані, що асоціюються з поточним об'єктом
