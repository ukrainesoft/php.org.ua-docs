---
navigation:
  - memcache.pconnect.md: '« Memcache::pconnect'
  - memcache.set.md: 'Memcache::set »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::replace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::replace

(PECL memcache >= 0.2.0)

Memcache::replace — Замінити значення наявного елемента

### Опис

```methodsynopsis
Memcache::replace(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
```

**Memcache::replace()** використовується для заміни значення існуючого елемента з цим ключем `key`. Якщо елемент з таким ключем не знайдено, **Memcache::replace()** повертає **`false`**. В інших випадках **Memcache::replace()** працює аналогічно [Memcache::set()](memcache.set.md). Ви також можете використати функцію **memcache\_replace()**

### Список параметрів

`key`

Ключ, пов'язаний із елементом.

`var`

Зберігається значення. Рядки та числа зберігаються так, інші типи серіалізуються.

`flag`

Используйте\*\*`MEMCACHE_COMPRESSED`\*\* для збереження елемента стисненим (використовується zlib).

`expire`

Термін життя елемент. Якщо дорівнює нулю, термін життя ніколи не спливе. Ви також можете використовувати тимчасову мітку Unix, або кількість секунд, починаючи з поточного часу, проте в цьому випадку кількість секунд не може бути більше 2592000 (30 днів).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Memcache::replace()\*\*\*\*

```php
<?php

$memcache_obj = memcache_connect('memcache_host', 11211);

/* процедурное API */
memcache_replace($memcache_obj, "test_key", "some variable", false, 30);

/* объектно-ориентированное API */
$memcache_obj->replace("test_key", "some variable", false, 30);

?>
```

### Дивіться також

-   [Memcache::set()](memcache.set.md) \- Зберегти дані на сервері
-   [Memcache::add()](memcache.add.md) \- Додати елемент із зазначеним ключем
