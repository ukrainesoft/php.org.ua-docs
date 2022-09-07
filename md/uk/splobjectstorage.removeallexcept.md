---
navigation:
  - splobjectstorage.removeall.md: '« SplObjectStorage::removeAll'
  - splobjectstorage.rewind.md: 'SplObjectStorage::rewind »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::removeAllExcept'
---
# SplObjectStorage::removeAllExcept

(PHP 5> = 5.3.6, PHP 7, PHP 8)

SplObjectStorage::removeAllExcept — Видаляє з поточного контейнера всі об'єкти, яких немає в іншому контейнері

### Опис

```methodsynopsis
public SplObjectStorage::removeAllExcept(SplObjectStorage $storage): int
```

Видаляє з поточного контейнера всі об'єкти, яких немає в іншому контейнері.

### Список параметрів

`storage`

Контейнер містить елементи, які повинні залишитися в поточному контейнері.

### Значення, що повертаються

Повертає кількість об'єктів, що залишилися.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::removeAllExcept()****

```php
<?php
$a = (object) 'a';
$b = (object) 'b';
$c = (object) 'c';

$foo = new SplObjectStorage;
$foo->attach($a);
$foo->attach($b);

$bar = new SplObjectStorage;
$bar->attach($b);
$bar->attach($c);

$foo->removeAllExcept($bar);
var_dump($foo->contains($a));
var_dump($foo->contains($b));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(false)
bool(true)
```
