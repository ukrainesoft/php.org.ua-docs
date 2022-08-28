Видаляє кілька записів із вказаного сервера

-   [« Memcached::deleteMulti](memcached.deletemulti.html)
    
-   [Memcached::fetch »](memcached.fetch.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Видаляє кілька записів із вказаного сервера
    

# Memcached::deleteMultiByKey

(PECL memcached >= 2.0.0)

Memcached::deleteMultiByKey — Видаляє кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::deleteMultiByKey(string $server_key, array $keys, int $time = 0): bool
```

**Memcached::deleteMultiByKey()** працює аналогічно [Memcached::deleteMulti()](memcached.deletemulti.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `keys` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`keys`

Ключ запису, що видаляється.

`time`

Час, протягом якого сервер очікує видалення запису.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTFOUND`** якщо заданий ключ не існує.

### Дивіться також

-   [Memcached::delete()](memcached.delete.html) - Видаляє запис
-   [Memcached::deleteByKey()](memcached.deletebykey.html) - Видаляє запис із вказаного сервера
-   [Memcached::deleteMulti()](memcached.deletemulti.html) - Видаляє кілька записів