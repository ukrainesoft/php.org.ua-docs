---
navigation:
  - memcached.getdelayed.md: '« Memcached::getDelayed'
  - memcached.getmulti.md: 'Memcached::getMulti »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getDelayedByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getDelayedByKey

(PECL memcached >= 0.1.0)

Memcached::getDelayedByKey — Запитує кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::getDelayedByKey(    string $server_key,    array $keys,    bool $with_cas = false,    ?callable $value_cb = null): bool
```

**Memcached::getDelayedByKey()** працює аналогічно [Memcached::getDelayed()](memcached.getdelayed.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`keys`

Масив із ключами для запиту записів.

`with_cas`

Чи запитувати CAS токени записів разом зі значеннями.

`value_cb`

Callback-Функция, возвращающая результат, или\*\*`null`\*\*

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### Дивіться також

-   [Memcached::getDelayed()](memcached.getdelayed.md) \- Запитує кілька записів
-   [Memcached::fetch()](memcached.fetch.md) \- Витягує наступний результат
-   [Memcached::fetchAll()](memcached.fetchall.md) \- Витягує всі отримані записи
