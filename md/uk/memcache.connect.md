---
navigation:
  - memcache.close.md: '« Memcache::close'
  - memcache.decrement.md: 'Memcache::decrement »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::connect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::connect

(PECL memcache >= 0.2.0)

Memcache::connect — Відкриває з'єднання з сервером memcached

### Опис

```methodsynopsis
Memcache::connect(string $host, int $port = ?, int $timeout = ?): bool
```

**Memcache::connect()** встановлює з'єднання з сервером memcached. З'єднання, відкрите за допомогою **Memcache::connect()**, автоматично закривається після закінчення скрипту. Також ви можете закрити з'єднання за допомогою [Memcache::close()](memcache.close.md). Також можна використовувати функцію **memcache\_connect()**

### Список параметрів

`host`

Визначає хост, на якому memcached чекає підключення. Цей параметр також може задавати інший транспорт, наприклад `unix:///path/to/memcached.sock` для використання сокетів Unix В такому випадку, `port` повинен бути заданий як

`port`

Визначає порт, на якому слухає memcached. Встановіть цей параметр рівним , якщо ви використовуєте сокети Unix.

Обратите внимание:`port`, если не задан, по умолчанию будет равен[memcache.default\_port](memcache.ini.md#ini.memcache.default-port). Тому має сенс вказати порт явно при виклику методу.

`timeout`

Значення в секундах, яке буде використано для підключення до демона. Двічі подумайте, перш ніж змінити значення за замовчуванням з 1 секунди – ви можете втратити всі переваги від кешування, якщо ваше з'єднання дуже повільне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::connect()\*\*\*\*

```php
<?php

/* процедурное API */

$memcache_obj = memcache_connect('memcache_host', 11211);

/* объектно-ориентированное API */

$memcache = new Memcache;
$memcache->connect('memcache_host', 11211);

?>
```

### Примітки

**Увага**

Якщо порт `port` не заданий, цей метод використовує значення за замовчуванням, задане в ini-налаштуванні [memcache.default\_port](memcache.ini.md#ini.memcache.default-port). Якщо це значення зміниться десь у вашому додатку, це може призвести до несподіваних результатів. Тому є сенс завжди вказати порт явно при виклику методу.

### Дивіться також

-   [Memcache::pconnect()](memcache.pconnect.md) \- Відкриває постійне з'єднання з сервером memcached
-   [Memcache::close()](memcache.close.md) \- Закрити з'єднання з сервером memcached
