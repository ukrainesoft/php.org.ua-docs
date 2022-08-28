Перекладає ітератор на перший елемент контейнера

-   [« SplObjectStorage::removeAllExcept](splobjectstorage.removeallexcept.html)
    
-   [SplObjectStorage::serialize »](splobjectstorage.serialize.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Перекладає ітератор на перший елемент контейнера
    

# SplObjectStorage::rewind

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання **SplObjectStorage::rewind()****

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
int(1)
int(0)
```

### Дивіться також

-   [SplObjectStorage::next()](splobjectstorage.next.html) - Перехід до наступного об'єкту