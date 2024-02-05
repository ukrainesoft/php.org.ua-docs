---
navigation:
  - memcached.touch.md: '« Memcached::touch'
  - class.memcachedexception.md: MemcachedException »
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::touchByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::touchByKey

(PECL memcached >= 2.0.0)

Memcached::touchByKey — Встановлює новий термін зберігання для запису на вказаному сервері

### Опис

```methodsynopsis
public Memcached::touchByKey(string $server_key, string $key, int $expiration = 0): bool
```

**Memcached::touchByKey()** працює аналогічно [Memcached::touch()](memcached.touch.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Дивіться також

-   [Memcached::touch()](memcached.touch.md) \- Встановлює новий термін зберігання для запису
