---
navigation:
  - memcached.getmulti.md: '« Memcached::getMulti'
  - memcached.getoption.md: 'Memcached::getOption »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getMultiByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getMultiByKey

(PECL memcached >= 0.1.0)

Memcached::getMultiByKey — Отримує кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::getMultiByKey(string $server_key, array $keys, int $get_flags = 0): array|false
```

**Memcached::getMultiByKey()** працює аналогічно [Memcached::getMulti()](memcached.getmulti.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`keys`

Масив із ключами для отримання записів.

`get_flags`

Прапори для отримання записів.

### Значення, що повертаються

Повертає масив знайдених записів або \*\*`false`\*\*в случае возникновения ошибки. Используйте при необходимости[Memcached::getResultCode()](memcached.getresultcode.md)

### список змін

| Версия | Опис |
| --- | --- |
| PECL memcached 3.0.0 | Видалено параметр `&cas_tokens`. . Додано константу **`Memcached::GET_EXTENDED`** для повернення токенів CAS. |

### Дивіться також

-   [Memcached::getMulti()](memcached.getmulti.md) \- Отримує кілька записів
-   [Memcached::get()](memcached.get.md) \- Отримання запису
-   [Memcached::getDelayed()](memcached.getdelayed.md) \- Запитує кілька записів
