---
navigation:
  - memcached.prepend.md: '« Memcached::prepend'
  - memcached.quit.md: 'Memcached::quit »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::prependByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::prependByKey

(PECL memcached >= 0.1.0)

Memcached::prependByKey — Додає дані на початок існуючого запису на вказаному сервері

### Опис

```methodsynopsis
public Memcached::prependByKey(string $server_key, string $key, string $value): ?bool
```

**Memcached::prependByKey()** працює аналогічно [Memcached::prepend()](memcached.prepend.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ запису до якого відбувається додавання на початок.

`value`

Доданий рядок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Повертає **`null`**, якщо стиснення увімкнено.

### Помилки

Повертає **`null`** та видає помилку рівня **`E_WARNING`**, якщо стиснення увімкнено.

### Дивіться також

-   [Memcached::prepend()](memcached.prepend.md) \- Додає дані на початок існуючого запису
-   [Memcached::append()](memcached.append.md) \- Додає дані до існуючого запису
