Видаляє об'єкт з контейнера

-   [« SplObjectStorage::current](splobjectstorage.current.html)
    
-   [SplObjectStorage::getHash »](splobjectstorage.gethash.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Видаляє об'єкт з контейнера
    

# SplObjectStorage::detach

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObjectStorage::detach — Видаляє об'єкт з контейнера.

### Опис

```methodsynopsis
public SplObjectStorage::detach(object $object): void
```

Видаляє об'єкт з контейнера.

### Список параметрів

`object`

Об'єкт об'єкта, що видаляється.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::detach()****

```php
<?php
$o = new StdClass;
$s = new SplObjectStorage();
$s->attach($o);
var_dump(count($s));
$s->detach($o);
var_dump(count($s));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
int(0)
```

### Дивіться також

-   [SplObjectStorage::attach()](splobjectstorage.attach.html) - Додає об'єкт у контейнер
-   [SplObjectStorage::removeAll()](splobjectstorage.removeall.html) - Видаляє з поточного контейнера об'єкти, які є в іншому контейнері