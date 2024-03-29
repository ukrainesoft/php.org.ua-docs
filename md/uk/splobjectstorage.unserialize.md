---
navigation:
  - splobjectstorage.setinfo.md: '« SplObjectStorage::setInfo'
  - splobjectstorage.valid.md: 'SplObjectStorage::valid »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::unserialize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::unserialize

(PHP 5 >= 5.2.2, PHP 7, PHP 8)

SplObjectStorage::unserialize — Відновлює серіалізований контейнер із рядка

### Опис

```methodsynopsis
public SplObjectStorage::unserialize(string $data): void
```

Відновлює дані контейнера з рядка та додає їх у поточний контейнер.

### Список параметрів

`data`

Серіалізоване подання контейнера.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::unserialize()\*\*\*\*

```php
<?php
$s1 = new SplObjectStorage;
$s2 = new SplObjectStorage;
$o = new stdClass;
$s1[$o] = "data";

$s2->unserialize($s1->serialize());

var_dump(count($s2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1)
```

### Дивіться також

-   [SplObjectStorage::serialize()](splobjectstorage.serialize.md) \- Серіалізує контейнер
