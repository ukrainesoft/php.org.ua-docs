---
navigation:
  - memcached.getstats.md: '« Memcached::getStats'
  - memcached.increment.md: 'Memcached::increment »'
  - index.md: PHP Manual
  - class.memcached.md: Memcached
title: 'Memcached::getVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Memcached::getVersion

(PECL memcached >= 0.1.5)

Memcached::getVersion — Отримує інформацію про версію серверів у пулі

### Опис

```methodsynopsis
public Memcached::getVersion(): array|false
```

**Memcached::getVersion()** повертає масив, що містить інформацію про версію кожного доступного сервера memcache.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Список масивів з інформацією про версію кожного сервера, де кожен елемент- окремий сервер.

### Приклади

**Пример #1 Пример использования**Memcached::getVersion()\*\*\*\*

```php
<?php
$m = new Memcached();
$m->addServer('localhost', 11211);

print_r($m->getVersion());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [localhost:11211] => 1.2.6
)
```
