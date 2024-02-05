---
navigation:
  - memcached.delete.md: '« Memcached::delete'
  - memcached.deletemulti.md: 'Memcached::deleteMulti »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::deleteByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::deleteByKey

(PECL memcached >= 0.1.0)

Memcached::deleteByKey — Видалення запису з вказаного сервера

### Опис

```methodsynopsis
public Memcached::deleteByKey(string $server_key, string $key, int $time = 0): bool
```

**Memcached::deleteByKey()** працює аналогічно [Memcached::delete()](memcached.delete.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ запису, що видаляється.

`time`

Період часу, протягом якого сервер очікує видалення запису.

> **Зауваження**: Починаючи з версії memcached 1.3.0 (випущена у 2009 році), функція більше не підтримується. Передача ненульового параметра `time` призведе до помилки при видаленні. Метод [Memcached::getResultCode()](memcached.getresultcode.md) поверне **`MEMCACHED_INVALID_ARGUMENTS`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Метод[Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо цей ключ не існує.

### Дивіться також

-   [Memcached::delete()](memcached.delete.md) \- Видаляє запис
-   [Memcached::deleteMulti()](memcached.deletemulti.md) \- Видаляє кілька записів
-   [Memcached::deleteMultiByKey()](memcached.deletemultibykey.md) \- Видаляє кілька записів із вказаного сервера
