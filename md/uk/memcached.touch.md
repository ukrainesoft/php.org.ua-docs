Встановлює новий термін зберігання для запису

-   [« Memcached::setSaslAuthData](memcached.setsaslauthdata.md)
    
-   [Memcached::touchByKey »](memcached.touchbykey.md)
    
-   [PHP Manual](index.md)
    
-   [Memcached](class.memcached.md)
    
-   Встановлює новий термін зберігання для запису
    

# Memcached::touch

(PECL memcached >= 2.0.0)

Memcached::touch — Встановлює новий термін зберігання для запису

### Опис

```methodsynopsis
public Memcached::touch(string $key, int $expiration): bool
```

**Memcached::touch()** встановлює новий термін зберігання для запису із зазначеним ключем.

### Список параметрів

`key`

Ключ, під яким зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Час зберігання об'єкту](memcached.expiration.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Використовуйте за необхідності [Memcached::getResultCode()](memcached.getresultcode.md)

### Дивіться також

-   [Memcached::touchByKey()](memcached.touchbykey.md) - Встановлює новий термін зберігання для запису на вказаному сервері