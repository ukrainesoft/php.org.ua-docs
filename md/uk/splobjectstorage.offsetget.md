---
navigation:
  - splobjectstorage.offsetexists.md: '« SplObjectStorage::offsetExists'
  - splobjectstorage.offsetset.md: 'SplObjectStorage::offsetSet »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::offsetGet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::offsetGet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetGet - Повертає дані, асоційовані з об'єктом object

### Опис

```methodsynopsis
public SplObjectStorage::offsetGet(object $object): mixed
```

Повертає дані, що асоціюються з об'єктом object.

### Список параметрів

`object`

Об'єкт об'єкта, що шукається.

### Значення, що повертаються

Дані, пов'язані з об'єктом object.

### Помилки

Викидає виняток [UnexpectedValueException](class.unexpectedvalueexception.md), якщо об'єкт `object` не вдалося знайти.

### Приклади

**Приклад #1 Приклад використання** SplObjectStorage::offsetGet()\*\*\*\*

```php
<?php
$s = new SplObjectStorage;

$o1 = new stdClass;
$o2 = new stdClass;

$s[$o1] = "hello";
$s->attach($o2);


var_dump($s->offsetGet($o1)); //  $s[$o1]
var_dump($s->offsetGet($o2)); //  $s[$o2]
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "hello"
NULL
```

### Дивіться також

-   [SplObjectStorage::offsetSet()](splobjectstorage.offsetset.md) \- Асоціює дані з об'єктом у контейнері
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) \- Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.md) \- Видаляє об'єкт із контейнера
