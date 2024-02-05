---
navigation:
  - memcached.set.md: '« Memcached::set'
  - memcached.setmulti.md: 'Memcached::setMulti »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::setByKey

(PECL memcached >= 0.1.0)

Memcached::setByKey — Зберігає запис на вказаному сервері

### Опис

```methodsynopsis
public Memcached::setByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = 0): bool
```

**Memcached::setByKey()** працює аналогічно [Memcached::set()](memcached.set.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Приклади

**Пример #1 Пример использования**Memcached::setByKey()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

/* Хранение блоков IP адресов на определённом сервере */
$m->setByKey('api-cache', 'block-ip:169.254.253.252', 1);
$m->setByKey('api-cache', 'block-ip:169.127.127.202', 1);
?>
```

### Дивіться також

-   [Memcached::set()](memcached.set.md) \- Зберігає запис
