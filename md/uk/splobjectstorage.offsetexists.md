---
navigation:
  - splobjectstorage.next.md: '« SplObjectStorage::next'
  - splobjectstorage.offsetget.md: 'SplObjectStorage::offsetGet »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::offsetExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::offsetExists

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetExists — Перевіряє, чи існує об'єкт у контейнері

### Опис

```methodsynopsis
public SplObjectStorage::offsetExists(object $object): bool
```

Перевіряє, чи об'єкт об'єкта існує в контейнері.

> **Зауваження** :
> 
> \*\*SplObjectStorage::offsetExists()\*\*является псевдонимом метода[SplObjectStorage::contains()](splobjectstorage.contains.md)

### Список параметрів

`object`

Об'єкт об'єкта, що шукається.

### Значення, що повертаються

Повертає **`true`**, якщо об'єкт object є у контейнері, та **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::offsetExists()\*\*\*\*

```php
<?php
$s = new SplObjectStorage;
$o1 = new stdClass;
$o2 = new stdClass;

$s->attach($o1);

var_dump($s->offsetExists($o1)); // аналогично isset($s[$o1])
var_dump($s->offsetExists($o2)); // аналогично isset($s[$o2])
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) \- Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.md) \- Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.md) \- Видаляє об'єкт із контейнера
