---
navigation:
  - splobjectstorage.offsetset.md: '« SplObjectStorage::offsetSet'
  - splobjectstorage.removeall.md: 'SplObjectStorage::removeAll »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::offsetUnset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::offsetUnset

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetUnset — Видаляє об'єкт із контейнера

### Опис

```methodsynopsis
public SplObjectStorage::offsetUnset(object $object): void
```

Видаляє об'єкт з контейнера.

> **Зауваження** :
> 
> \*\*SplObjectStorage::offsetUnset()\*\*является псевдонимом метода[SplObjectStorage::detach()](splobjectstorage.detach.md)

### Список параметрів

`object`

Об'єкт об'єкта, що видаляється.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::offsetUnset()\*\*\*\*

```php
<?php
$o = new stdClass;
$s = new SplObjectStorage();
$s->attach($o);
var_dump(count($s));
$s->offsetUnset($o); // аналогично unset($s[$o])
var_dump(count($s));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
int(0)
```

### Дивіться також

-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.md) \- Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) \- Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) \- Перевіряє, чи існує об'єкт у контейнері
