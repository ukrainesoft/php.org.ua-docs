Видалити елемент із сервера

-   [« Memcache::decrement](memcache.decrement.html)
    
-   [Memcache::flush »](memcache.flush.html)
    
-   [PHP Manual](index.html)
    
-   [Memcache](class.memcache.html)
    
-   Видалити елемент із сервера
    

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

Це застарілий параметр і зараз не використовується. Значення за замовчуванням `0` секунд. Не використовуйте цей параметр.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| Невідомо | Не рекомендується використовувати параметр `timeout`. Поведінка буде різнитися в різних версіях memcache, однак його встановлення в `0` безпечна. Інші значення цього параметра можуть призвести до помилок під час видалення елемента. |

### Приклади

**Приклад #1 Приклад використання **Memcache::delete()****

```php
<?php

/* процедурное API */
$memcache_obj = memcache_connect('memcache_host', 11211);

/* элемент будет удалён сервером */
memcache_delete($memcache_obj, 'key_to_delete');

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->connect('memcache_host', 11211);

$memcache_obj->delete('key_to_delete');

?>
```

### Дивіться також

-   [Memcache::set()](memcache.set.html) - Зберегти дані на сервері
-   [Memcache::replace()](memcache.replace.html) - Замінити значення наявного елемента