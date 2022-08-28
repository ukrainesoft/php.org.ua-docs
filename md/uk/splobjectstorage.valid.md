Визначає, чи допустиме поточне значення ітератора

-   [« SplObjectStorage::unserialize](splobjectstorage.unserialize.html)
    
-   [Итераторы »](spl.iterators.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Визначає, чи допустиме поточне значення ітератора
    

# SplObjectStorage::valid

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання **SplObjectStorage::valid()****

```php
<?php
$s = new SplObjectStorage();

$o1 = new StdClass;
$o2 = new StdClass;

$s->attach($o1, "d1");
$s->attach($o2, "d2");

$s->rewind();
while($s->valid()) {
    echo $s->key()."\n";
    $s->next();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
0
1
```

### Дивіться також

-   [SplObjectStorage::current()](splobjectstorage.current.html) - Повертає поточний об'єкт
-   [SplObjectStorage::getInfo()](splobjectstorage.getinfo.html) - Повертає дані, що асоціюються з поточним об'єктом