Перевіряє, чи контейнер містить заданий об'єкт

-   [« SplObjectStorage::attach](splobjectstorage.attach.md)
    
-   [SplObjectStorage::count »](splobjectstorage.count.md)
    
-   [PHP Manual](index.md)
    
-   [SplObjectStorage](class.splobjectstorage.md)
    
-   Перевіряє, чи контейнер містить заданий об'єкт
    

# SplObjectStorage::contains

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObjectStorage::contains — Перевіряє, чи контейнер містить заданий об'єкт

### Опис

```methodsynopsis
public SplObjectStorage::contains(object $object): bool
```

Перевіряє, чи контейнер містить заданий об'єкт object.

### Список параметрів

`object`

Об'єкт об'єкта, що шукається.

### Значення, що повертаються

Повертає **`true`**, якщо object знаходиться в контейнері, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::contains()****

```php
<?php
$o1 = new StdClass;
$o2 = new StdClass;

$s = new SplObjectStorage();

$s[$o1] = "hello";
var_dump($s->contains($o1));
var_dump($s->contains($o2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) - Перевіряє, чи існує об'єкт у контейнері