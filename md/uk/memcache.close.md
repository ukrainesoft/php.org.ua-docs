---
navigation:
  - memcache.addserver.md: '« Memcache::addServer'
  - memcache.connect.md: 'Memcache::connect »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::close

(PECL memcache >= 0.4.0)

Memcache::close — Закрити з'єднання з сервером memcached

### Опис

```methodsynopsis
Memcache::close(): bool
```

**Memcache::close()** закриває з'єднання з сервером memcached. Ця функція не закриває постійне з'єднання, яке закривається лише під час завершення роботи/перезапуску веб-сервера. Ви також можете використати функцію **memcache\_close()**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**Memcache::close()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);
/*
сделать что-нибудь здесь...
*/
memcache_close($memcache_obj);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);
/*
сделать что-нибудь здесь...
*/
$memcache_obj->close();

?>
```

### Дивіться також

-   [Memcache::connect()](memcache.connect.md) \- Відкриває з'єднання з сервером memcached
-   [Memcache::pconnect()](memcache.pconnect.md) \- Відкриває постійне з'єднання з сервером memcached
