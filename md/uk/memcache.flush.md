---
navigation:
  - memcache.delete.md: '« Memcache::delete'
  - memcache.get.md: 'Memcache::get »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::flush'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::flush

(PECL memcache >= 1.0.0)

Memcache::flush — Скинути всі існуючі елементи на сервері

### Опис

```methodsynopsis
Memcache::flush(): bool
```

**Memcache::flush()** негайно анулює всі існуючі елементи . **Memcache::flush()** практично не звільняє ресурси, лише позначає все елементи як минулі, тому зайнята пам'ять буде перезаписана новими елементами. Ви також можете використовувати функцію **memcache\_flush()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::flush()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);

memcache_flush($memcache_obj);

/* объектно-ориентированное API */

$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);

$memcache_obj->flush();

?>
```
