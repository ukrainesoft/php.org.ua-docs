Видаляє об'єкт із контейнера

-   [« SplObjectStorage::offsetSet](splobjectstorage.offsetset.html)
    
-   [SplObjectStorage::removeAll »](splobjectstorage.removeall.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Видаляє об'єкт із контейнера
    

# SplObjectStorage::offsetUnset

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetUnset — Видаляє об'єкт із контейнера

### Опис

```methodsynopsis
public SplObjectStorage::offsetUnset(object $object): void
```

Видаляє об'єкт з контейнера.

> **Зауваження**
> 
> **SplObjectStorage::offsetUnset()** є псевдонімом методу [SplObjectStorage::detach()](splobjectstorage.detach.html)

### Список параметрів

`object`

Об'єкт об'єкта, що видаляється.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::offsetUnset()****

```php
<?php
$o = new StdClass;
$s = new SplObjectStorage();
$s->attach($o);
var_dump(count($s));
$s->offsetUnset($o); // аналогично unset($s[$o])
var_dump(count($s));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
int(0)
```

### Дивіться також

-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.html) - Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.html) - Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.html) - Перевіряє, чи існує об'єкт у контейнері