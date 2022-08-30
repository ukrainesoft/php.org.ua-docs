Додає дані на початок існуючого запису на вказаному сервері

-   [« Memcached::prepend](memcached.prepend.md)
    
-   [Memcached::quit »](memcached.quit.md)
    
-   [PHP Manual](index.md)
    
-   [Memcached](class.memcached.md)
    
-   Додає дані на початок існуючого запису на вказаному сервері
    

# Memcached::prependByKey

(PECL memcached >= 0.1.0)

Memcached::prependByKey — Додає дані на початок існуючого запису на вказаному сервері

### Опис

```methodsynopsis
public Memcached::prependByKey(string $server_key, string $key, string $value): bool
```

**Memcached::prependByKey()** працює аналогічно [Memcached::prepend()](memcached.prepend.md), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`key`

Ключ запису до якого відбувається додавання на початок.

`value`

Доданий рядок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає **`Memcached::RES_NOTSTORED`** якщо переданий ключ не існує.

### Дивіться також

-   [Memcached::prepend()](memcached.prepend.md) - Додає дані на початок існуючого запису
-   [Memcached::append()](memcached.append.md) - Додає дані до існуючого запису