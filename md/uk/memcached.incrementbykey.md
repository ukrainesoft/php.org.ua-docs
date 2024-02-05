---
navigation:
  - memcached.increment.md: '« Memcached::increment'
  - memcached.ispersistent.md: 'Memcached::isPersistent »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::incrementByKey'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::incrementByKey

(PECL memcached >= 2.0.0)

Memcached::incrementByKey — Збільшує числове значення запису, що зберігається на вказаному сервері

### Опис

```methodsynopsis
public Memcached::incrementByKey(    string $server_key,    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
```

**Memcached::incrementByKey()** збільшує числове значення запису на величину, вказану у параметрі `offset`. Якщо значення запису не є числовим, то повернеться помилка . \*\*Memcached::incrementByKey()\*\*установит записи значение параметра`initial_value` якщо переданого ключа немає.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування по ключу самого елемента, при виборі сервера, що підключається, memcached хешують по ключу сервера. Такий метод дозволяє групувати пов'язані елементи разом на одному сервері, що підвищує ефективність групових операцій.

`key`

Ключ запису, що збільшується

`offset`

Величина, на яку відбувається збільшення значення запису.

`initial_value`

Ініціює значення, яке буде встановлено запису, якщо переданого ключа немає.

`expiry`

Час, коли термін дії запису спливає.

### Значення, що повертаються

Повертає нове значення запису у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [Memcached::decrement()](memcached.decrement.md) \- Зменшує числове значення запису
-   [Memcached::decrementByKey()](memcached.decrementbykey.md) \- Зменшує числове значення запису, що зберігається на певному сервері
-   [Memcached::increment()](memcached.increment.md) \- Збільшує числове значення запису
