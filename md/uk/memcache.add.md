Додати елемент із зазначеним ключем

-   [« Memcache](class.memcache.md)
    
-   [Memcache::addServer »](memcache.addserver.md)
    
-   [PHP Manual](index.md)
    
-   [Memcache](class.memcache.md)
    
-   Додати елемент із зазначеним ключем
    

# Memcache::add

(PECL memcache >= 0.2.0)

Memcache::add — Додати елемент із зазначеним ключем

### Опис

```methodsynopsis
Memcache::add(    string $key,    mixed $var,    int $flag = ?,    int $expire = ?): bool
```

**Memcache::add()** записує елемент `var` із зазначеним ключем `key` тільки якщо цей ключ ще не існує на сервері. Також можна використовувати функцію **memcacheadd()**

### Список параметрів

`key`

Ключ, з яким пов'язаний елемент.

`var`

Змінна для збереження. Рядкові та числові значення зберігаються як є, інші типи серіалізуються.

`flag`

Використовуйте **`MEMCACHE_COMPRESSED`** для запису елемента зі стисненням (використовується zlib).

`expire`

Час життя елемент. Якщо дорівнює нулю, елемент ніколи не старіє. Також ви можете використовувати мітку часу Unix або число секунд, починаючи з поточного моменту, однак, у цьому випадку число секунд не може бути більше 2592000 (30 днів).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає \*\*`false`\*\*якщо такий ключ вже існує. В інших випадках поведінка **Memcache::add()** аналогічно [Memcache::set()](memcache.set.md)

### Приклади

**Приклад #1 Приклад використання **Memcache::add()****

```php
<?php

$memcache_obj = memcache_connect("localhost", 11211);

/* процедурное API */
memcache_add($memcache_obj, 'var_key', 'test variable', false, 30);

/* объектно-ориентированное API */
$memcache_obj->add('var_key', 'test variable', false, 30);

?>
```

### Дивіться також

-   [Memcache::set()](memcache.set.md) - Зберегти дані на сервері
-   [Memcache::replace()](memcache.replace.md) - Замінити значення наявного елемента