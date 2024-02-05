---
navigation:
  - memcached.append.md: '« Memcached::append'
  - memcached.cas.md: 'Memcached::cas »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::appendByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::appendByKey

(PECL memcached >= 0.1.0)

Memcached::appendByKey — Додає дані до наявного запису на заданому сервері

### Опис

```methodsynopsis
public Memcached::appendByKey(string $server_key, string $key, string $value): ?bool
```

**Memcached::appendByKey()** працює аналогічно методу [Memcached::append()](memcached.append.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та установки `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`value`

Рядок для додавання до кінця існуючого запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає **`null`**, якщо стиснення увімкнено.

### Помилки

Повертає **`null`** та видає помилку рівня **`E_WARNING`**, якщо стиснення увімкнено.

### Дивіться також

-   [Memcached::append()](memcached.append.md) \- Додає дані до існуючого запису
-   [Memcached::prepend()](memcached.prepend.md) \- Додає дані на початок існуючого запису
