Повертає об'єкт кошика із бригади для подальшої роботи з ним

-   [« streambucketappend](function.stream-bucket-append.html)
    
-   [streambucketnew »](function.stream-bucket-new.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з потоками](ref.stream.md)
    
-   Повертає об'єкт кошика із бригади для подальшої роботи з ним
    

# streambucketmakewriteable

(PHP 5, PHP 7, PHP 8)

streambucketmakewriteable — Повертає об'єкт кошика із бригади для подальшої роботи з ним

### Опис

```methodsynopsis
stream_bucket_make_writeable(resource $brigade): ?object
```

Функція викликається щоразу, коли виникає необхідність у доступі до вмісту, що міститься в бригаді та роботі з ним. Зазвичай функція викликається з [phpuserfilter::filter()](php-user-filter.filter.html)

### Список параметрів

`brigade`

Бригада, з якої необхідно повернути об'єкт кошика.

### Значення, що повертаються

Повертає об'єкт кошика з властивостями, наведеними нижче або **`null`**

data (string)

`data` `bucket` Поточний рядок у кошику.

datalen (integer)

`datalen` `bucket` Довжина рядка у кошику.

### Дивіться також

-   [streambucketappend()](function.stream-bucket-append.html) - Додати відро (bucket) до бригади (brigade)
-   [streambucketprepend()](function.stream-bucket-prepend.html) - Додати відро на початок бригади