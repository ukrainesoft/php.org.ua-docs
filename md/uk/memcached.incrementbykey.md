Збільшує числове значення запису, що зберігається на вказаному сервері

-   [« Memcached::increment](memcached.increment.html)
    
-   [Memcached::isPersistent »](memcached.ispersistent.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Збільшує числове значення запису, що зберігається на вказаному сервері
    

# Memcached::incrementByKey

(PECL memcached >= 2.0.0)

Memcached::incrementByKey — Збільшує числове значення запису, що зберігається на вказаному сервері

### Опис

```methodsynopsis
public Memcached::incrementByKey(    string $server_key,    string $key,    int $offset = 1,    int $initial_value = 0,    int $expiry = 0): int|false
```

**Memcached::incrementByKey()** збільшує числове значення запису на величину, вказану у параметрі `offset`. Якщо значення запису не є числовим, то повернеться помилка . **Memcached::incrementByKey()** встановить запису значення параметра `initial_value` якщо переданого ключа немає.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ запису, що збільшується

`offset`

Величина, на яку відбувається збільшення значення запису.

`initial_value`

Ініціює значення, яке буде встановлено запису, якщо переданого ключа немає.

`expiry`

Час, коли термін дії запису спливає.

### Значення, що повертаються

Повертає нове значення запису у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Memcached::decrement()](memcached.decrement.html) - Зменшує числове значення запису
-   [Memcached::decrementByKey()](memcached.decrementbykey.html) - Зменшує числове значення запису, що зберігається на певному сервері
-   [Memcached::increment()](memcached.increment.html) - Збільшує числове значення запису