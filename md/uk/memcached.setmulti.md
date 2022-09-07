---
navigation:
  - memcached.setbykey.md: '« Memcached::setByKey'
  - memcached.setmultibykey.md: 'Memcached::setMultiByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setMulti'
---
# Memcached::setMulti

(PECL memcached >= 0.1.0)

Memcached::setMulti — Зберігає кілька записів

### Опис

```methodsynopsis
public Memcached::setMulti(array $items, int $expiration = ?): bool
```

**Memcached::setMulti()** схожий на метод [Memcached::set()](memcached.set.md), але замість однієї пари ключ/значення, працює з кількома записами, переданими в `items` у вигляді масиву. Параметр `expiration`, що встановлює термін зберігання запису, застосовується до всіх записів.

### Список параметрів

`items`

Зберігається масив пар ключів/значень.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Приклад #1 Приклад використання **Memcached::setMulti()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

$items = array(
    'key1' => 'value1',
    'key2' => 'value2',
    'key3' => 'value3'
);
$m->setMulti($items, time() + 300);
?>
```

### Дивіться також

-   [Memcached::setMultiByKey()](memcached.setmultibykey.md) - Зберігає кілька записів на вказаному сервері
-   [Memcached::set()](memcached.set.md) - Зберігає запис
