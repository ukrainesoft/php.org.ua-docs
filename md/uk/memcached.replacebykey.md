---
navigation:
  - memcached.replace.html: '« Memcached::replace'
  - memcached.resetserverlist.html: 'Memcached::resetServerList »'
  - index.html: PHP Manual
  - class.memcached.html: Memcached
title: 'Memcached::replaceByKey'
---
# Memcached::replaceByKey

(PECL memcached >= 0.1.0)

Memcached::replaceByKey — Замінює існуючий запис із заданим ключем на вказаному сервері

### Опис

```methodsynopsis
public Memcached::replaceByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = ?): bool
```

**Memcached::replaceByKey()** працює аналогічно [Memcached::replace()](memcached.replace.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTSTORED`** якщо вказаного ключа немає.

### Дивіться також

-   [Memcached::replace()](memcached.replace.html) - Замінює існуючий запис із зазначеним ключем
-   [Memcached::set()](memcached.set.html) - Зберігає запис
-   [Memcached::add()](memcached.add.html) - Додає елемент із новим ключем
