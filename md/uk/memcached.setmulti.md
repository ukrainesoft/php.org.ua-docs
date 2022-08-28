Зберігає кілька записів

-   [« Memcached::setByKey](memcached.setbykey.html)
    
-   [Memcached::setMultiByKey »](memcached.setmultibykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Зберігає кілька записів
    

# Memcached::setMulti

(PECL memcached >= 0.1.0)

Memcached::setMulti — Зберігає кілька записів

### Опис

```methodsynopsis
public Memcached::setMulti(array $items, int $expiration = ?): bool
```

**Memcached::setMulti()** схожий на метод [Memcached::set()](memcached.set.html), але замість однієї пари ключ/значення, працює з кількома записами, переданими в `items` у вигляді масиву. Параметр `expiration`, що встановлює термін зберігання запису, застосовується до всіх записів.

### Список параметрів

`items`

Зберігається масив пар ключів/значень.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Время хранения объекта](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### Приклади

**Приклад #1 Приклад використання **Memcached::setMulti()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items, time() + 300);
?>
```

### Дивіться також

-   [Memcached::setMultiByKey()](memcached.setmultibykey.html) - Зберігає кілька записів на вказаному сервері
-   [Memcached::set()](memcached.set.html) - Зберігає запис