Порівнює та встановлює значення для запису

-   [« Memcached::appendByKey](memcached.appendbykey.html)
    
-   [Memcached::casByKey »](memcached.casbykey.html)
    
-   [PHP Manual](index.html)
    
-   [Memcached](class.memcached.html)
    
-   Порівнює та встановлює значення для запису
    

# Memcached::cas

(PECL memcached >= 0.1.0)

Memcached::cas — Порівнює та встановлює значення для запису

### Опис

```methodsynopsis
public Memcached::cas(    float $cas_token,    string $key,    mixed $value,    int $expiration = ?): bool
```

**Memcached::cas()** здійснює перевірку та встановлення значення запису, нове значення буде збережено тільки якщо інші клієнти не оновили його з часу останнього звернення цим клієнтом. Ця перевірка здійснюється за допомогою параметра `cas_token`, який являє собою 64-бітове значення, присвоєне існуючому запису сервером memcache. Зверніться до документації методу **Memcached::get**який використовується для отримання цього токена. Зверніть увагу, що токен представлений у вигляді числа подвійної точності через обмеження діапазону значень цілого типу в PHP.

### Список параметрів

`cas_token`

Унікальне значення, пов'язане із існуючим записом. Генерується сервером memcache.

`key`

Ключ, під яким зберігається значення.

`value`

Зберігається значення.

`expiration`

Час зберігання об'єкта за промовчанням дорівнює 0. Для більш детальної інформації дивіться [Время хранения объекта](memcached.expiration.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Метод [Memcached::getResultCode()](memcached.getresultcode.html) повертає **`Memcached::RES_DATA_EXISTS`** якщо запис, який ви намагаєтеся зберегти, було змінено з моменту останнього звернення.

### Приклади

**Приклад #1 Приклад використання **Memcached::cas()****

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

do {
    /* fetch IP list and its token */
    $ips = $m->get('ip_block', null, $cas);
    /* if list doesn't exist yet, create it and do
       an atomic add which will fail if someone else already added it */
    if ($m->getResultCode() == Memcached::RES_NOTFOUND) {
        $ips = array($_SERVER['REMOTE_ADDR']);
        $m->add('ip_block', $ips);
    /* otherwise, add IP to the list and store via compare-and-swap
       with the token, which will fail if someone else updated the list */
    } else {
        $ips[] = $_SERVER['REMOTE_ADDR'];
        $m->cas($cas, 'ip_block', $ips);
    }
} while ($m->getResultCode() != Memcached::RES_SUCCESS);

?>
```

### Дивіться також

-   [Memcached::casByKey()](memcached.casbykey.html) - Порівнює та встановлює значення для запису на конкретному сервері