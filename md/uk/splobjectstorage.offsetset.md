---
navigation:
  - splobjectstorage.offsetget.md: '« SplObjectStorage::offsetGet'
  - splobjectstorage.offsetunset.md: 'SplObjectStorage::offsetUnset »'
  - index.md: PHP Manual
  - class.splobjectstorage.md: SplObjectStorage
title: 'SplObjectStorage::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SplObjectStorage::offsetSet

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::offsetSet — Асоціює дані з об'єктом у контейнері

### Опис

```methodsynopsis
public SplObjectStorage::offsetSet(object $object, mixed $info = null): void
```

Асоціює дані з об'єктом об'єкта в контейнері.

> **Зауваження** :
> 
> \*\*SplObjectStorage::offsetSet()\*\*является псевдонимом метода[SplObjectStorage::attach()](splobjectstorage.attach.md)

### Список параметрів

`object`

Об'єкт об'єкта з яким потрібно зв'язати дані.

`info`

Дані, які потрібно зв'язати з об'єктом об'єкта.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**SplObjectStorage::offsetSet()\*\*\*\*

```php
<?php
$s = new SplObjectStorage;

$o1 = new stdClass;

$s->offsetSet($o1, "hello"); // $s[$o1] = "hello";

var_dump($s[$o1]);
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "hello"
```

### Дивіться також

-   [SplObjectStorage::attach()](splobjectstorage.attach.md) \- Додає об'єкт у контейнер
-   [SplObjectStorage::offsetGet()](splobjectstorage.offsetget.md) \- Повертає дані, асоційовані з об'єктом object
-   [SplObjectStorage::offsetExists()](splobjectstorage.offsetexists.md) \- Перевіряє, чи існує об'єкт у контейнері
-   [SplObjectStorage::offsetUnset()](splobjectstorage.offsetunset.md) \- Видаляє об'єкт із контейнера
