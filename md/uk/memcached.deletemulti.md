---
navigation:
  - memcached.deletebykey.md: '« Memcached::deleteByKey'
  - memcached.deletemultibykey.md: 'Memcached::deleteMultiByKey »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::deleteMulti'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::deleteMulti

(PECL memcached >= 2.0.0)

Memcached::deleteMulti — Видаляє кілька записів

### Опис

```methodsynopsis
public Memcached::deleteMulti(array $keys, int $time = 0): array
```

Видаляє записи, передані в масиві `keys`с сервера.

### Список параметрів

`keys`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

> **Зауваження**: Починаючи з версії memcached 1.3.0 (випущена у 2009 році), функція більше не підтримується. Передача ненульового параметра `time` призведе до помилки при видаленні. Метод [Memcached::getResultCode()](memcached.getresultcode.md) поверне **`MEMCACHED_INVALID_ARGUMENTS`**

### Значення, що повертаються

Повертає масив із індексами `keys` і значеннями, що позначають вдало чи ні, завершилася операція. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ немає.

### Дивіться також

-   [Memcached::delete()](memcached.delete.md) \- Видаляє запис
-   [Memcached::deleteByKey()](memcached.deletebykey.md) \- Видаляє запис із вказаного сервера
-   [Memcached::deleteMultiByKey()](memcached.deletemultibykey.md) \- Видаляє кілька записів із вказаного сервера
