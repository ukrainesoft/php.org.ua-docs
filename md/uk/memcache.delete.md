---
navigation:
  - memcache.decrement.md: '« Memcache::decrement'
  - memcache.flush.md: 'Memcache::flush »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::delete'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::delete

(PECL memcache >= 0.2.0)

Memcache::delete — Видалити елемент із сервера

### Опис

```methodsynopsis
Memcache::delete(string $key, int $timeout = 0): bool
```

**Memcache::delete()** видаляє елемент із зазначеним ключем `key`

### Список параметрів

`key`

Ключ елемента, що видаляється.

`timeout`

Це застарілий параметр і зараз не використовується. Значення за замовчуванням секунд. Не використовуйте цей параметр.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| Невідомо | Не рекомендується використовувати параметр `timeout`. . Поведінка буде різнитися в різних версіях memcache, однак його встановлення в безпечна. Інші значення цього параметра можуть призвести до помилок під час видалення елемента. |

### Приклади

**Пример #1 Пример использования**Memcache::delete()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);

/* элемент будет удалён сервером */
memcache_delete($memcache_obj, 'key_to_delete');

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);

$memcache_obj->delete('key_to_delete');

?>
```

### Дивіться також

-   [Memcache::set()](memcache.set.md) \- Зберегти дані на сервері
-   [Memcache::replace()](memcache.replace.md) \- Замінити значення наявного елемента
