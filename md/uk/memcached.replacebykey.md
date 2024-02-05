---
navigation:
  - memcached.replace.md: '« Memcached::replace'
  - memcached.resetserverlist.md: 'Memcached::resetServerList »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::replaceByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::replaceByKey

(PECL memcached >= 0.1.0)

Memcached::replaceByKey — Замінює існуючий запис із заданим ключем на вказаному сервері

### Опис

```methodsynopsis
public Memcached::replaceByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = 0): bool
```

**Memcached::replaceByKey()** працює аналогічно [Memcached::replace()](memcached.replace.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTSTORED`** якщо вказаного ключа немає.

### Дивіться також

-   [Memcached::replace()](memcached.replace.md) \- Замінює існуючий запис із зазначеним ключем
-   [Memcached::set()](memcached.set.md) \- Зберігає запис
-   [Memcached::add()](memcached.add.md) \- Додає елемент із новим ключем
