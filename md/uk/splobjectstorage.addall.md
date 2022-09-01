---
navigation:
  - class.splobjectstorage.md: « SplObjectStorage
  - splobjectstorage.attach.md: 'SplObjectStorage::attach »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::addAll'
---
# SplObjectStorage::addAll

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplObjectStorage::addAll — Додає всі об'єкти з іншого контейнера

### Опис

```methodsynopsis
public SplObjectStorage::addAll(SplObjectStorage $storage): int
```

Додає всі пари об'єкт-дані з іншого контейнера у поточний.

### Список параметрів

`storage`

Контейнер об'єктів, з якого потрібно імпортувати дані.

### Значення, що повертаються

Кількість об'єктів у сховищі.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::addAll()****

```php
<?php
$o = new StdClass;
$a = new SplObjectStorage();
$a[$o] = "hello";

$b = new SplObjectStorage();
$b->addAll($a);
echo $b[$o]."\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
hello
```

### Дивіться також

-   [SplObjectStorage::removeAll()](splobjectstorage.removeall.md) - Видаляє з поточного контейнера об'єкти, які є в іншому контейнері
