Асоціює дані з об'єктом у контейнері

-   [« SplObjectStorage::offsetGet](splobjectstorage.offsetget.html)
    
-   [SplObjectStorage::offsetUnset »](splobjectstorage.offsetunset.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Асоціює дані з об'єктом у контейнері
    

# SplObjectStorage::offsetSet

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetSet — Асоціює дані з об'єктом у контейнері

### Опис

```methodsynopsis
public SplObjectStorage::offsetSet(object $object, mixed $info = null): void
```

Асоціює дані з об'єктом об'єкта в контейнері.

> **Зауваження**
> 
> **SplObjectStorage::offsetSet()** є псевдонімом методу [SplObjectStorage::attach()](splobjectstorage.attach.html)

### Список параметрів

`object`

Об'єкт об'єкта з яким потрібно зв'язати дані.

`info`

Дані, які потрібно зв'язати з об'єктом об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::offsetSet()****

```php
<?php
$s = new SplObjectStorage;

$o1 = new StdClass;

$s->offsetSet($o1, "hello"); // $s[$o1] = "hello";

var_dump($s[$o1]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "hello"
```

### Дивіться також

-   [SplObjectStorage::attach()](splobjectstorage.attach.html) - Додає об'єкт у контейнер
-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.html) - Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.html) - Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.html) - Видаляє об'єкт із контейнера