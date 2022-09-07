---
navigation:
  - memcached.getallkeys.md: '« Memcached::getAllKeys'
  - memcached.getdelayed.md: 'Memcached::getDelayed »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getByKey'
---
# Memcached::getByKey

(PECL memcached >= 0.1.0)

Memcached::getByKey — Отримує запис із певного сервера

### Опис

```methodsynopsis
public Memcached::getByKey(    string $server_key,    string $key,    callable $cache_cb = ?,    int $flags = ?): mixed
```

**Memcached::getByKey()** працює аналогічно [Memcached::get()](memcached.get.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ одержуваного запису.

`cache_cb`

Callback-функція для читання, що кешується, або **`null`**

`flags`

Прапори визначають повертається результат. Якщо містить **`Memcached::GET_EXTENDED`**, то буде повернуто токен CAS.

### Значення, що повертаються

Повертає значення, що зберігається в кеші або **`false`** в іншому випадку. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTFOUND`** якщо переданий ключ не існує.

### список змін

| Версия | Описание |
| --- | --- |
| PECL memcached 3.0.0 | Видалено параметр `&cas_token`. Замість нього додано параметр `flags`, в який можна передати значення **`Memcached::GET_EXTENDED`** для того, щоб було повернуто токен CAS. |

### Дивіться також

-   [Memcached::get()](memcached.get.md) - Отримання запису
-   [Memcached::getMulti()](memcached.getmulti.md) - Отримує кілька записів
-   [Memcached::getDelayed()](memcached.getdelayed.md) - Запитує кілька записів
