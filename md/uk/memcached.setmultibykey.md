Зберігає кілька записів на вказаному сервері

-   [« Memcached::setMulti](memcached.setmulti.html)
    
-   [Memcached::setOption »](memcached.setoption.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Зберігає кілька записів на вказаному сервері
    

# Memcached::setMultiByKey

(PECL memcached >= 0.1.0)

Memcached::setMultiByKey — Зберігає кілька записів на вказаному сервері

### Опис

```methodsynopsis
public Memcached::setMultiByKey(string $server_key, array $items, int $expiration = ?): bool
```

**Memcached::setMultiByKey()** працює аналогічно [Memcached::setMulti()](memcached.setmulti.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер. Це корисно, коли необхідно тримати кілька пов'язаних значень на конкретному сервері.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`items`

Зберігається масив пар ключів/значень.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### Дивіться також

-   [Memcached::setMulti()](memcached.setmulti.html) - Зберігає кілька записів
-   [Memcached::set()](memcached.set.html) - Зберігає запис