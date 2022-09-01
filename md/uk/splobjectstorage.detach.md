---
navigation:
  - splobjectstorage.current.md: '« SplObjectStorage::current'
  - splobjectstorage.gethash.md: 'SplObjectStorage::getHash »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::detach'
---
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

-   [SplObjectStorage::attach()](splobjectstorage.attach.md) - Додає об'єкт у контейнер
-   [SplObjectStorage::removeAll()](splobjectstorage.removeall.md) - Видаляє з поточного контейнера об'єкти, які є в іншому контейнері
