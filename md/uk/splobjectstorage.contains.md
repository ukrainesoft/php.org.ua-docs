---
navigation:
  - splobjectstorage.attach.md: '« SplObjectStorage::attach'
  - splobjectstorage.count.md: 'SplObjectStorage::count »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::contains'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::contains

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

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

**Приклад #1 Приклад використання** SplObjectStorage::contains()\*\*\*\*

```php
<?php
$o1 = new stdClass;
$o2 = new stdClass;

$s = new SplObjectStorage();

$s[$o1] = "hello";
var_dump($s->contains($o1));
var_dump($s->contains($o2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) \- Перевіряє, чи існує об'єкт у контейнері
