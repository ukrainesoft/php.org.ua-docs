Відновлює серіалізований контейнер із рядка

-   [« SplObjectStorage::setInfo](splobjectstorage.setinfo.html)
    
-   [SplObjectStorage::valid »](splobjectstorage.valid.html)
    
-   [PHP Manual](index.html)
    
-   [SplObjectStorage](class.splobjectstorage.html)
    
-   Відновлює серіалізований контейнер із рядка
    

# SplObjectStorage::unserialize

(PHP 5> = 5.2.2, PHP 7, PHP 8)

SplObjectStorage::unserialize — Відновлює серіалізований контейнер із рядка

### Опис

```methodsynopsis
public SplObjectStorage::unserialize(string $data): void
```

Відновлює дані контейнера з рядка та додає їх у поточний контейнер.

### Список параметрів

`data`

Серіалізоване представлення контейнера.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::unserialize()****

```php
<?php
$s1 = new SplObjectStorage;
$s2 = new SplObjectStorage;
$o = new StdClass;
$s1[$o] = "data";

$s2->unserialize($s1->serialize());

var_dump(count($s2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```

### Дивіться також

-   [SplObjectStorage::serialize()](splobjectstorage.serialize.html) - Серіалізує контейнер