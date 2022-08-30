Додає елемент із новим ключем

-   [« Memcached](class.memcached.md)
    
-   [Memcached::addByKey »](memcached.addbykey.md)
    
-   [PHP Manual](index.md)
    
-   [Memcached](class.memcached.md)
    
-   Додає елемент із новим ключем
    

# Memcached::add

(PECL memcached >= 0.1.0)

Memcached::add — Додає елемент із новим ключем

### Опис

```methodsynopsis
public Memcached::add(string $key, mixed $value, int $expiration = ?): bool
```

Метод **Memcached::add()** схожий на [Memcached::set()](memcached.set.md), але операція додавання завершиться помилкою, якщо ключ `key` вже існує на сервері.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.md) повертає \*\*`Memcached::RES_NOTSTORED`\*\*якщо переданий ключ вже існує.

### Дивіться також

-   [Memcached::addByKey()](memcached.addbykey.md) - Додає новий елемент на заданий сервер
-   [Memcached::set()](memcached.set.md) - Зберігає запис
-   [Memcached::replace()](memcached.replace.md) - Замінює існуючий запис із зазначеним ключем