Повертає дані, що асоціюються з поточним об'єктом

-   [« SplObjectStorage::getHash](splobjectstorage.gethash.md)
    
-   [SplObjectStorage::key »](splobjectstorage.key.md)
    
-   [PHP Manual](index.md)
    
-   [SplObjectStorage](class.splobjectstorage.md)
    
-   Повертає дані, що асоціюються з поточним об'єктом
    

# SplObjectStorage::getInfo

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::getInfo — Повертає дані, пов'язані з поточним об'єктом

### Опис

```methodsynopsis
public SplObjectStorage::getInfo(): mixed
```

Повертає дані, асоційовані з об'єктом, на який вказує ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дані, пов'язані з об'єктом.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::getInfo()****

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

-   [SplObjectStorage::current()](splobjectstorage.current.md) - Повертає поточний об'єкт
-   [SplObjectStorage::rewind()](splobjectstorage.rewind.md) - Переводить ітератор на перший елемент контейнера
-   [SplObjectStorage::key()](splobjectstorage.key.md) - Повертає індекс поточного становища ітератора
-   [SplObjectStorage::next()](splobjectstorage.next.md) - Перехід до наступного об'єкту
-   [SplObjectStorage::valid()](splobjectstorage.valid.md) - Визначає, чи допустиме поточне значення ітератора
-   [SplObjectStorage::setInfo()](splobjectstorage.setinfo.md) - Асоціює дані з поточним об'єктом контейнера