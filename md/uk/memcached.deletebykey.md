Видаляє запис із вказаного сервера

-   [« Memcached::delete](memcached.delete.html)
    
-   [Memcached::deleteMulti »](memcached.deletemulti.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Видаляє запис із вказаного сервера
    

# Memcached::deleteByKey

(PECL memcached >= 0.1.0)

Memcached::deleteByKey — Видалення запису з вказаного сервера

### Опис

```methodsynopsis
public Memcached::deleteByKey(string $server_key, string $key, int $time = 0): bool
```

**Memcached::deleteByKey()** працює аналогічно [Memcached::delete()](memcached.delete.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ запису, що видаляється.

`time`

Період часу, протягом якого сервер очікує видалення запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTFOUND`** якщо цей ключ не існує.

### Дивіться також

-   [Memcached::delete()](memcached.delete.html) - Видаляє запис
-   [Memcached::deleteMulti()](memcached.deletemulti.html) - Видаляє кілька записів
-   [Memcached::deleteMultiByKey()](memcached.deletemultibykey.html) - Видаляє кілька записів із вказаного сервера