Встановлює новий термін зберігання для запису на вказаному сервері

-   [« Memcached::touch](memcached.touch.html)
    
-   [MemcachedException »](class.memcachedexception.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Встановлює новий термін зберігання для запису на вказаному сервері
    

# Memcached::touchByKey

(PECL memcached >= 2.0.0)

Memcached::touchByKey — Встановлює новий термін зберігання для запису на вказаному сервері

### Опис

```methodsynopsis
public Memcached::touchByKey(string $server_key, string $key, int $expiration): bool
```

**Memcached::touchByKey()** працює аналогічно [Memcached::touch()](memcached.touch.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ, під яким зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Время хранения объекта](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### Дивіться також

-   [Memcached::touch()](memcached.touch.html) - Встановлює новий термін зберігання для запису