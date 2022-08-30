Перевіряє, чи існує об'єкт у контейнері

-   [« SplObjectStorage::next](splobjectstorage.next.md)
    
-   [SplObjectStorage::offsetGet »](splobjectstorage.offsetget.md)
    
-   [PHP Manual](index.md)
    
-   [SplObjectStorage](class.splobjectstorage.md)
    
-   Перевіряє, чи існує об'єкт у контейнері
    

# SplObjectStorage::offsetExists

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetExists — Перевіряє, чи існує об'єкт у контейнері

### Опис

```methodsynopsis
public SplObjectStorage::offsetExists(object $object): bool
```

Перевіряє, чи об'єкт об'єкта існує в контейнері.

> **Зауваження**
> 
> **SplObjectStorage::offsetExists()** є псевдонімом методу [SplObjectStorage::contains()](splobjectstorage.contains.md)

### Список параметрів

`object`

Об'єкт об'єкта, що шукається.

### Значення, що повертаються

Повертає **`true`**, якщо об'єкт object є у контейнері, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::offsetExists()****

```php
<?php
$s = new SplObjectStorage;
$o1 = new StdClass;
$o2 = new StdClass;

$s->attach($o1);

var_dump($s->offsetExists($o1)); // аналогично isset($s[$o1])
var_dump($s->offsetExists($o2)); // аналогично isset($s[$o2])
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) - Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.md) - Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.md) - Видаляє об'єкт із контейнера