---
navigation:
  - splobjectstorage.addall.md: '« SplObjectStorage::addAll'
  - splobjectstorage.contains.md: 'SplObjectStorage::contains »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::attach'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::attach

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

SplObjectStorage::attach — Додає об'єкт у контейнер

### Опис

```methodsynopsis
public SplObjectStorage::attach(object $object, mixed $info = null): void
```

Додає об'єкт object в контейнер і може додатково асоціювати цей об'єкт з якимись даними.

### Список параметрів

`object`

Об'єкт object, що додається.

`info`

Дані, із якими потрібно асоціювати об'єкт object.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**SplObjectStorage::attach()\*\*\*\*

```php
<?php
$o1 = new stdClass;
$o2 = new stdClass;
$s = new SplObjectStorage();
$s->attach($o1); // то же, что и $s[$o1] = NULL;
$s->attach($o2, "hello"); // то же, что и $s[$o2] = "hello";

var_dump($s[$o1]);
var_dump($s[$o2]);

?>
```

Висновок наведеного прикладу буде схожим на:

```
NULL
string(5) "hello"
```

### Дивіться також

-   [SplObjectStorage::detach()](splobjectstorage.detach.md) \- Видаляє об'єкт object із контейнера
-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) \- Асоціює дані з об'єктом у контейнері
