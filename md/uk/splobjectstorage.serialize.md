---
navigation:
  - splobjectstorage.rewind.md: '« SplObjectStorage::rewind'
  - splobjectstorage.setinfo.md: 'SplObjectStorage::setInfo »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::serialize'
---
# SplObjectStorage::serialize

(PHP 5> = 5.2.2, PHP 7, PHP 8)

SplObjectStorage::serialize — Серіалізує контейнер

### Опис

```methodsynopsis
public SplObjectStorage::serialize(): string
```

Повертає рядкову виставу контейнера.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядкове представлення контейнера.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::serialize()****

```php
<?php
$s = new SplObjectStorage;
$o = new StdClass;
$s[$o] = "data";

echo $s->serialize()."\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
x:i:1;O:8:"stdClass":0:{},s:4:"data";;m:a:0:{}
```

### Дивіться також

-   [SplObjectStorage::unserialize()](splobjectstorage.unserialize.md) - Відновлює серіалізований контейнер із рядка
