---
navigation:
  - memcache.increment.md: '« Memcache::increment'
  - memcache.replace.md: 'Memcache::replace »'
  - index.md: PHP Manual
  - class.memcache.md: Memcache
title: 'Memcache::pconnect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcache::pconnect

(PECL memcache >= 0.4.0)

Memcache::pconnect — Відкриває постійне з'єднання з сервером memcached

### Опис

```methodsynopsis
Memcache::pconnect(string $host, int $port = ?, int $timeout = ?): mixed
```

\*\*Memcache::pconnect()\*\*аналогична[Memcache::connect()](memcache.connect.md) з тією різницею, що з'єднання встановлюється незмінним. Це з'єднання не закривається після завершення виконання скрипту та функцією [Memcache::close()](memcache.close.md). Ви також можете використати функцію **memcache\_pconnect()**

### Список параметрів

`host`

Вказує на хост, на якому memcached прослуховує з'єднання. Цей параметр також може вказувати на інший транспорт, такий як `unix:///path/to/memcached.sock`, для використання сокетів домену UNIX, у цьому випадку `port`должен установлен в

`port`

Вказує на порт, на якому memcached прослуховує з'єднання. Встановіть цей параметр на коли використовуються сокети домену UNIX.

`timeout`

Значення в секундах, яке використовуватиметься для підключення до домену. Подумайте двічі, перш ніж змінювати значення за замовчуванням в 1 секунду - ви можете втратити всі переваги кешування, якщо з'єднання занадто повільне.

### Значення, що повертаються

Повертає об'єкт Memcache або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcache::pconnect()\*\*\*\*

```php
<?php

/* процедурное API */
$memcache_obj = memcache_pconnect('memcache_host', 11211);

/* объектно-ориентированное API */
$memcache_obj = new Memcache;
$memcache_obj->pconnect('memcache_host', 11211);

?>
```

### Дивіться також

-   [Memcache::connect()](memcache.connect.md) \- Відкриває з'єднання з сервером memcached
