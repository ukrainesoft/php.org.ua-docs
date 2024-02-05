---
navigation:
  - memcached.add.md: '« Memcached::add'
  - memcached.addserver.md: 'Memcached::addServer »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::addByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::addByKey

(PECL memcached >= 0.1.0)

Memcached::addByKey — Додає новий елемент на заданий сервер

### Опис

```methodsynopsis
public Memcached::addByKey(    string $server_key,    string $key,    mixed $value,    int $expiration = 0): bool
```

**Memcached::addByKey()** працює аналогічно [Memcached::add()](memcached.add.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає \*\*`Memcached::RES_NOTSTORED`\*\*якщо переданий ключ вже існує.

### Дивіться також

-   [Memcached::add()](memcached.add.md) \- Додає елемент із новим ключем
-   [Memcached::set()](memcached.set.md) \- Зберігає запис
-   [Memcached::replace()](memcached.replace.md) \- Замінює існуючий запис із зазначеним ключем
