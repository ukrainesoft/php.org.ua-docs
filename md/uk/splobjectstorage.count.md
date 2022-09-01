---
navigation:
  - splobjectstorage.contains.md: '« SplObjectStorage::contains'
  - splobjectstorage.current.md: 'SplObjectStorage::current »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::count'
---
# SplObjectStorage::count

(PHP 5> = 5.1.0, PHP 7, PHP 8)

SplObjectStorage::count — Повертає кількість об'єктів у контейнері

### Опис

```methodsynopsis
public SplObjectStorage::count(int $mode = COUNT_NORMAL): int
```

Здійснює підрахунок об'єктів у контейнері.

### Список параметрів

`mode`

Якщо для необов'язкового параметра `mode` встановлено значення **`COUNT_RECURSIVE`** (або 1), **SplObjectStorage::count()** рекурсивно підраховуватиме обсяг сховища.

### Значення, що повертаються

Кількість об'єктів у контейнері.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::count()****

```php
<?php
$s = new SplObjectStorage();
$o1 = new StdClass;
$o2 = new StdClass;

$s->attach($o1);
$s->attach($o2);
$s->attach($o1);
var_dump($s->count());
var_dump(count($s));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(2)
int(2)
```

### Дивіться також

-   [SplObjectStorage::attach()](splobjectstorage.attach.md) - Додає об'єкт у контейнер
-   [SplObjectStorage::detach()](splobjectstorage.detach.md) - Видаляє об'єкт object із контейнера
