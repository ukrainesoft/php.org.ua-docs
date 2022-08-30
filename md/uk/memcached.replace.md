Замінює існуючий запис із зазначеним ключем

-   [« Memcached::quit](memcached.quit.html)
    
-   [Memcached::replaceByKey »](memcached.replacebykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Замінює існуючий запис із зазначеним ключем
    

# Memcached::replace

(PECL memcached >= 0.1.0)

Memcached::replace — Замінює існуючий запис із зазначеним ключем

### Опис

```methodsynopsis
public Memcached::replace(string $key, mixed $value, int $expiration = ?): bool
```

**Memcached::replace()** схожий на метод [Memcached::set()](memcached.set.html), але операція завершиться невдачею у випадку, якщо ключ `key` відсутня на сервері.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_NOTSTORED`** якщо вказаного ключа немає.

### Дивіться також

-   [Memcached::replaceByKey()](memcached.replacebykey.html) - Замінює існуючий запис із заданим ключем на вказаному сервері
-   [Memcached::set()](memcached.set.html) - Зберігає запис
-   [Memcached::add()](memcached.add.html) - Додає елемент із новим ключем