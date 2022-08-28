Отримує кілька записів із вказаного сервера

-   [« Memcached::getMulti](memcached.getmulti.html)
    
-   [Memcached::getOption »](memcached.getoption.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Отримує кілька записів із вказаного сервера
    

# Memcached::getMultiByKey

(PECL memcached >= 0.1.0)

Memcached::getMultiByKey — Отримує кілька записів із вказаного сервера

### Опис

```methodsynopsis
public Memcached::getMultiByKey(string $server_key, array $keys, int $flags = ?): array|false
```

**Memcached::getMultiByKey()** працює аналогічно [Memcached::getMulti()](memcached.getmulti.html), за винятком того, що довільний `server_key` може бути використаний для визначення сервера та встановлення значення з ключем `key` на конкретний сервер.

### Список параметрів

`server_key`

Ключ, що ідентифікує сервер, де зберігається значення. Замість хешування за ключем самого елемента, ми хешуємо по ключу сервера при виборі сервера, що підключається, memcached. Цей підхід дозволяє групувати зв'язані елементи разом на одному сервері, що покращує ефективність групових операцій.

`keys`

Масив із ключами для отримання записів.

`flags`

Прапори для отримання записів.

### Значення, що повертаються

Повертає масив знайдених записів або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.html)

### список змін

| Версия | Описание |
| --- | --- |
| PECL memcached 3.0.0 | Видалено параметр `&cas_tokens`. Додано константу **`Memcached::GET_EXTENDED`** для повернення токенів CAS. |

### Дивіться також

-   [Memcached::getMulti()](memcached.getmulti.html) - Отримує кілька записів
-   [Memcached::get()](memcached.get.html) - Отримання запису
-   [Memcached::getDelayed()](memcached.getdelayed.html) - Запитує кілька записів