Повертає дані, асоційовані з об'єктом object

-   [« SplObjectStorage::offsetExists](splobjectstorage.offsetexists.html)
    
-   [SplObjectStorage::offsetSet »](splobjectstorage.offsetset.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Повертає дані, асоційовані з об'єктом object
    

# SplObjectStorage::offsetGet

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetGet - Повертає дані, асоційовані з об'єктом object

### Опис

```methodsynopsis
public SplObjectStorage::offsetGet(object $object): mixed
```

Повертає дані, що асоціюються з об'єктом object.

### Список параметрів

`object`

Об'єкт об'єкта, що шукається.

### Значення, що повертаються

Дані, пов'язані з об'єктом object.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.html), якщо об'єкт `object` не вдалося знайти.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::offsetGet()****

```php
<?php
$s = new SplObjectStorage;

$o1 = new StdClass;
$o2 = new StdClass;

$s[$o1] = "hello";
$s->attach($o2);


var_dump($s->offsetGet($o1)); //  $s[$o1]
var_dump($s->offsetGet($o2)); //  $s[$o2]
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(5) "hello"
NULL
```

### Дивіться також

-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.html) - Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.html) - Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.html) - Видаляє об'єкт із контейнера