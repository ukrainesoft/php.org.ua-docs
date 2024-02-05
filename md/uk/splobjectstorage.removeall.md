---
navigation:
  - splobjectstorage.offsetunset.md: '« SplObjectStorage::offsetUnset'
  - splobjectstorage.removeallexcept.md: 'SplObjectStorage::removeAllExcept »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::removeAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::removeAll

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::removeAll — Видаляє з поточного контейнера об'єкти, які є в іншому контейнері

### Опис

```methodsynopsis
public SplObjectStorage::removeAll(SplObjectStorage $storage): int
```

Видаляє з поточного контейнера об'єкти, які є в іншому контейнері.

### Список параметрів

`storage`

Контейнер містить елементи, які потрібно видалити.

### Значення, що повертаються

Повертає кількість об'єктів, що залишилися.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::removeAll()\*\*\*\*

```php
<?php
$o1 = new stdClass;
$o2 = new stdClass;
$a = new SplObjectStorage();
$a[$o1] = "foo";

$b = new SplObjectStorage();
$b[$o1] = "bar";
$b[$o2] = "gee";

var_dump(count($b));
$b->removeAll($a);
var_dump(count($b));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(2)
int(1)
```

### Дивіться також

-   [SplObjectStorage::addAll()](splobjectstorage.addall.md) \- Додає всі об'єкти з іншого контейнера
