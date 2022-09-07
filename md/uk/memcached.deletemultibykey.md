---
navigation:
  - memcached.deletemulti.md: '« Memcached::deleteMulti'
  - memcached.fetch.md: 'Memcached::fetch »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::deleteMultiByKey'
---
# Memcached::deleteMultiByKey

(PECL memcached >= 2.0.0)

Memcached::deleteMultiByKey — Видаляє кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::deleteMultiByKey(string $server_key, array $keys, int $time = 0): bool
```

**Memcached::deleteMultiByKey()** працює аналогічно [Memcached::deleteMulti()](memcached.deletemulti.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `keys` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`keys`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ не існує.

### Дивіться також

-   [Memcached::delete()](memcached.delete.md) - Видаляє запис
-   [Memcached::deleteByKey()](memcached.deletebykey.md) - Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti()](memcached.deletemulti.md) - Видаляє кілька записів
