---
navigation:
  - memcached.decrement.md: '« Memcached::decrement'
  - memcached.delete.md: 'Memcached::delete »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::decrementByKey'
---
# Memcached::decrementByKey

(PECL memcached >= 2.0.0)

Memcached::decrementByKey — Зменшує числове значення запису, що зберігається на певному сервері

### Опис

```methodsynopsis
public Memcached::decrementByKey(    string $server_key,    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
```

**Memcached::decrementByKey()** зменшує числове значення запису на величину задану в `offset`. Якщо значення запису не є числовим, буде повернено помилку. Якщо функція зменшить значення запису менше нуля, буде встановлено нульове значення . **Memcached::decrementByKey()** встановить запису значення параметра `initial_value` якщо переданого ключа немає.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ запису, що зменшується.

`offset`

Величина, на яку зменшується значення запису.

`initial_value`

Ініціює значення запису, якщо ключа не існує.

`expiry`

Час, коли термін дії запису спливає.

### Значення, що повертаються

Повертає нове значення запису у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Memcached::decrement()](memcached.decrement.md) - Зменшує числове значення запису
-   [Memcached::increment()](memcached.increment.md) - Збільшує числове значення запису
-   [Memcached::incrementByKey()](memcached.incrementbykey.md) - Збільшує числове значення запису, що зберігається на вказаному сервері
