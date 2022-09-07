---
navigation:
  - memcache.setcompressthreshold.md: '« Memcache::setCompressThreshold'
  - ref.memcache.md: Функции Memcache »
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::setServerParams'
---
# Memcache::setServerParams

(PECL memcache >= 2.1.0)

Memcache::setServerParams — Змінює параметри сервера та статус під час виконання

### Опис

```methodsynopsis
Memcache::setServerParams(    string $host,    int $port = 11211,    int $timeout = ?,    int $retry_interval = false,    bool $status = ?,    callable $failure_callback = ?): bool
```

**Memcache::setServerParams()** змінює параметри сервера під час виконання. Ви також можете використати функцію **memcachesetserverparams()**

> **Зауваження**
> 
> Ця функція була додана до Memcache версії 2.1.0.

### Список параметрів

`host`

Вказує на хост, на якому memcached прослуховує з'єднання.

`port`

Вказує на порт, на якому memcached прослуховує з'єднання.

`timeout`

Значення в секундах, яке використовуватиметься для підключення до домену. Подумайте двічі, перш ніж змінювати значення за замовчуванням в 1 секунду - ви можете втратити всі переваги кешування, якщо з'єднання занадто повільне.

`retry_interval`

Керує частотою перевірки доступності сервера, що відмовив, за замовчуванням 15 секунд. Якщо встановити значення "-1", то спроб перевірити доступність сервера робитися не буде. Ні цей параметр, ні параметр `persistent` не впливають, якщо модуль завантажений динамічно через функцію [dl()](function.dl.md)

`status`

Визначає, чи сервер позначений прапором як "онлайн". Встановлення цього параметра **`false`** і `retry_interval` -1 дозволить зберегти сервер в пулі, але не використовувати його в алгоритмі розподілу ключів. Запит до цього сервера або запустить механізм забезпечення стійкості до відмов, або відразу ж перерветься з помилкою, залежно від налаштування `memcache.allow_failover`. За замовчуванням одно \*\*`true`\*\*що означає, що сервер активний і готовий приймати запити.

`failure_callback`

Дозволяє користувачеві задати callback-функцію, яка запуститься у разі будь-якої помилки. Ця функція буде викликана раніше, ніж буде запущено механізм забезпечення стійкості до відмови. Функція приймає два параметри - ім'я хоста і порт сервера, що відмовив.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Memcache::setServerParams()****

```php
<?php

function _callback_memcache_failure($host, $port) {
    print "неудачное подключение memcache - '$host:$port'";
}

/* объектно-ориентированное API */

$memcache = new Memcache;

// Добавить сервер в офлайн-режим
$memcache->addServer('memcache_host', 11211, false, 1, 1, -1, false);

// Перевести сервер обратно в онлайн
$memcache->setServerParams('memcache_host', 11211, 1, 15, true, '_callback_memcache_failure');

/* процедурное API */

$memcache_obj = memcache_connect('memcache_host', 11211);
memcache_set_server_params($memcache_obj, 'memcache_host', 11211, 1, 15, true, '_callback_memcache_failure');

?>
```

### Дивіться також

-   [Memcache::addServer()](memcache.addserver.md) - Додає сервер memcached в пул з'єднань
-   [Memcache::getServerStatus()](memcache.getserverstatus.md) - Повертає статус сервера
