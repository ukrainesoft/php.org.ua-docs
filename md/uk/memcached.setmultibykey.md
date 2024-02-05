---
navigation:
  - memcached.setmulti.md: '« Memcached::setMulti'
  - memcached.setoption.md: 'Memcached::setOption »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::setMultiByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::setMultiByKey

(PECL memcached >= 0.1.0)

Memcached::setMultiByKey — Зберігає кілька записів на вказаному сервері

### Опис

```methodsynopsis
public Memcached::setMultiByKey(string $server_key, array $items, int $expiration = 0): bool
```

**Memcached::setMultiByKey()** працює аналогічно [Memcached::setMulti()](memcached.setmulti.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`items`

Зберігається масив пар ключів/значень.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Дивіться також

-   [Memcached::setMulti()](memcached.setmulti.md) \- Зберігає кілька записів
-   [Memcached::set()](memcached.set.md) \- Зберігає запис
