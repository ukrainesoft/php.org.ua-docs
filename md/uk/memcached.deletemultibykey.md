---
navigation:
  - memcached.deletemulti.md: '« Memcached::deleteMulti'
  - memcached.fetch.md: 'Memcached::fetch »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::deleteMultiByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::deleteMultiByKey

(PECL memcached >= 2.0.0)

Memcached::deleteMultiByKey — Видаляє кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::deleteMultiByKey(string $server_key, array $keys, int $time = 0): array
```

**Memcached::deleteMultiByKey()** працює аналогічно [Memcached::deleteMulti()](memcached.deletemulti.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `keys` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`keys`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

> **Зауваження**: Починаючи з версії memcached 1.3.0 (випущена у 2009 році), функція більше не підтримується. Передача ненульового параметра `time` призведе до помилки при видаленні. Метод [Memcached::getResultCode()](memcached.getresultcode.md) поверне **`MEMCACHED_INVALID_ARGUMENTS`**

### Значення, що повертаються

Повертає масив, проіндексований ключами `keys`. Кожен елемент дорівнює **`true`**, якщо відповідний ключ був видалений або однією з констант \*\*`Memcached::RES_*`\*\*якщо при видаленні виникла помилка.

Метод[Memcached::getResultCode()](memcached.getresultcode.md) поверне код результату для останньої виконаної операції видалення, тобто операції видалення для останнього елемента `keys`

### Дивіться також

-   [Memcached::delete()](memcached.delete.md) \- Видаляє запис
-   [Memcached::deleteByKey()](memcached.deletebykey.md) \- Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti()](memcached.deletemulti.md) \- Видаляє кілька записів
