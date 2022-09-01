---
navigation:
  - splobjectstorage.serialize.md: '« SplObjectStorage::serialize'
  - splobjectstorage.unserialize.md: 'SplObjectStorage::unserialize »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::setInfo'
---
# SplObjectStorage::setInfo

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::setInfo — Асоціює дані з поточним об'єктом контейнера

### Опис

```methodsynopsis
public SplObjectStorage::setInfo(mixed $info): void
```

Асоціює дані з поточним об'єктом контейнера, на який вказує ітератор.

### Список параметрів

`info`

Дані, які потрібно зв'язати із поточним об'єктом.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::setInfo()****

```php
<?php
$s = new SplObjectStorage();

$o1 = new StdClass;
$o2 = new StdClass;

$s->attach($o1, "d1");
$s->attach($o2, "d2");

$s->rewind();
while($s->valid()) {
    $s->setInfo("new");
    $s->next();
}
var_dump($s[$o1]);
var_dump($s[$o2]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(3) "new"
string(3) "new"
```

### Дивіться також

-   [SplObjectStorage::current()](splobjectstorage.current.md) - Повертає поточний об'єкт
-   [SplObjectStorage::rewind()](splobjectstorage.rewind.md) - перекладає ітератор на перший елемент контейнера
-   [SplObjectStorage::key()](splobjectstorage.key.md) - Повертає індекс поточного становища ітератора
-   [SplObjectStorage::next()](splobjectstorage.next.md) - Перехід до наступного об'єкту
-   [SplObjectStorage::valid()](splobjectstorage.valid.md) - Визначає, чи допустиме поточне значення ітератора
-   [SplObjectStorage::getInfo()](splobjectstorage.getinfo.md) - Повертає дані, що асоціюються з поточним об'єктом
