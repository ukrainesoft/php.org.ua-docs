Додає елемент із новим ключем

-   [« Memcached](class.memcached.html)
    
-   [Memcached::addByKey »](memcached.addbykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Додає елемент із новим ключем
    

# Memcached::add

(PECL memcached >= 0.1.0)

Memcached::add — Додає елемент із новим ключем

### Опис

```methodsynopsis
public Memcached::add(string $key, mixed $value, int $expiration = ?): bool
```

Метод **Memcached::add()** схожий на [Memcached::set()](memcached.set.html), але операція додавання завершиться помилкою, якщо ключ `key` вже існує на сервері.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Время хранения объекта](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає \*\*`Memcached::RES_NOTSTORED`\*\*якщо переданий ключ вже існує.

### Дивіться також

-   [Memcached::addByKey()](memcached.addbykey.html) - Додає новий елемент на заданий сервер
-   [Memcached::set()](memcached.set.html) - Зберігає запис
-   [Memcached::replace()](memcached.replace.html) - Замінює існуючий запис із зазначеним ключем