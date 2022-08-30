Відкриває з'єднання з сервером memcached

-   [« Memcache::close](memcache.close.md)
    
-   [Memcache::decrement »](memcache.decrement.md)
    
-   [PHP Manual](index.md)
    
-   [Memcache](class.memcache.md)
    
-   Відкриває з'єднання з сервером memcached
    

# Memcache::connect

(PECL memcache >= 0.2.0)

Memcache::connect — Відкриває з'єднання з сервером memcached

### Опис

```methodsynopsis
Memcache::connect(string $host, int $port = ?, int $timeout = ?): bool
```

**Memcache::connect()** встановлює з'єднання з сервером memcached. З'єднання, відкрите за допомогою **Memcache::connect()**, автоматично закривається після закінчення скрипту. Також ви можете закрити з'єднання за допомогою [Memcache::close()](memcache.close.md). Також можна використовувати функцію **memcacheconnect()**

### Список параметрів

`host`

Визначає хост, на якому memcached чекає підключення. Цей параметр також може задавати інший транспорт, наприклад `unix:///path/to/memcached.sock` для використання сокетів Unix В такому випадку, `port` повинен бути заданий як `0`

`port`

Визначає порт, на якому слухає memcached. Встановіть цей параметр рівним `0`, якщо ви використовуєте сокети Unix.

Зверніть увагу: `port`, якщо не заданий, за замовчуванням дорівнюватиме [memcache.defaultport](memcache.ini.html#ini.memcache.default-port). Тому має сенс вказати порт явно при виклику методу.

`timeout`

Значення в секундах, яке буде використано для підключення до демона. Двічі подумайте, перш ніж змінити значення за замовчуванням з 1 секунди – ви можете втратити всі переваги від кешування, якщо ваше з'єднання дуже повільне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::connect()****

```php
<?php

/* процедурное API */

$memcache_obj = memcache_connect('memcache_host', 11211);

/* объектно-ориентированное API */

$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);

?>
```

### Примітки

**Увага**

Якщо порт `port` не заданий, цей метод використовує значення за замовчуванням, задане в ini-налаштуванні [memcache.defaultport](memcache.ini.html#ini.memcache.default-port). Якщо це значення зміниться десь у вашому додатку, це може призвести до несподіваних результатів. Тому сенс завжди вказати порт явно при виклику методу.

### Дивіться також

-   [Memcache::pconnect()](memcache.pconnect.md) - Відкриває постійне з'єднання з сервером memcached
-   [Memcache::close()](memcache.close.md) - Закрити з'єднання з сервером memcached