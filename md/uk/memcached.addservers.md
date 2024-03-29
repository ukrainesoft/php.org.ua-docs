---
navigation:
  - memcached.addserver.md: '« Memcached::addServer'
  - memcached.append.md: 'Memcached::append »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::addServers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::addServers

(PECL memcached >= 0.1.1)

Memcached::addServers — Додає кілька серверів у пул

### Опис

```methodsynopsis
public Memcached::addServers(array $servers): bool
```

**Memcached::addServers()** додає сервери, вказані в масиві `servers`, у загальний пул. Кожен елемент масиву `servers` є масивом, що містить ім'я хоста, порт і, необов'язково, ваговий коефіцієнт сервера. З'єднання з серверами не встановлюється.

Один і той самий сервер може зустрічатися в пулі кілька разів, тому що жодних перевірок на дублювання входжень немає. Але це недоцільно; натомість потрібно використовувати параметр `weight` підвищення пріоритету даного сервера.

### Список параметрів

`array`

Масив із серверами для додавання в пул.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** Memcached::addServers()\*\*\*\*

```php
<?php
$m = new Memcached();

$servers = array(
    array('mem1.domain.com', 11211, 33),
    array('mem2.domain.com', 11211, 67)
);
$m->addServers($servers);
?>
```

### Дивіться також

-   [Memcached::addServer()](memcached.addserver.md) \- Додає сервер у пул
-   [Memcached::resetServerList()](memcached.resetserverlist.md) \- Очищає список серверів
