---
navigation:
  - splobjectstorage.offsetset.md: '« SplObjectStorage::offsetSet'
  - splobjectstorage.removeall.md: 'SplObjectStorage::removeAll »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::offsetUnset'
---
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
> **SplObjectStorage::offsetUnset()** є псевдонімом методу [SplObjectStorage::detach()](splobjectstorage.detach.md)

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

-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.md) - Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) - Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) - Перевіряє, чи існує об'єкт у контейнері
