Запитує кілька записів із вказаного сервера

-   [« Memcached::getDelayed](memcached.getdelayed.html)
    
-   [Memcached::getMulti »](memcached.getmulti.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Запитує кілька записів із вказаного сервера
    

# Memcached::getDelayedByKey

(PECL memcached >= 0.1.0)

Memcached::getDelayedByKey — Запитує кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::getDelayedByKey(    string $server_key,    array $keys,    bool $with_cas = ?,    callable $value_cb = ?): bool
```

**Memcached::getDelayedByKey()** працює аналогічно [Memcached::getDelayed()](memcached.getdelayed.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`keys`

Масив із ключами для запиту записів.

`with_cas`

Чи запитувати CAS токени записів разом зі значеннями.

`value_cb`

Callback-Функція, що повертає результат, або **`null`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### Дивіться також

-   [Memcached::getDelayed()](memcached.getdelayed.html) - Запитує кілька записів
-   [Memcached::fetch()](memcached.fetch.html) - Витягує наступний результат
-   [Memcached::fetchAll()](memcached.fetchall.html) - Витягує всі отримані записи