---
navigation:
  - zookeeperconfig.add.md: '« ZookeeperConfig::add'
  - zookeeperconfig.remove.md: 'ZookeeperConfig::remove »'
  - index.md: PHP Manual
  - class.zookeeperconfig.md: ZookeeperConfig
title: 'ZookeeperConfig::get'
---
# ZookeeperConfig::get

(PECL zookeeper >= 0.6.0, ZooKeeper >= 3.5.0)

ZookeeperConfig::get — Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключений клієнт

### Опис

```methodsynopsis
public
   ZookeeperConfig::get(callable $watcher_cb = null, array &$stat = null): string
```

### Список параметрів

`watcher_cb`

Якщо не нуль, на сервері буде встановлено спостерігач, щоб повідомляти клієнта, коли вузол змінюється.

`stat`

Якщо не NULL, буде містити значення stat для шляху повернення.

### Значення, що повертаються

Повертає рядок конфігурації у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод генерує [ZookeeperException](class.zookeeperexception.md) та його похідні, коли кількість параметрів або типи неправильні або не вдається отримати конфігурацію.

### Приклади

**Приклад #1 Приклад використання **ZookeeperConfig::get()****

Отримання конфігурації.

```php
<?php
$zk = new Zookeeper();
$zk->connect('localhost:2181');
$zk->addAuth('digest', 'timandes:timandes');
$zkConfig = $zk->getConfig();
$r = $zkConfig->get();
if ($r)
  echo $r;
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
server.1=localhost:2888:3888:participant;0.0.0.0:2181
version=0xca01e881a2
```

### Дивіться також

-   [ZookeeperConfig::set()](zookeeperconfig.set.md) - Змінює склад ансамблю ZK та ролі його учасників
-   [ZookeeperConfig::add()](zookeeperconfig.add.md) - Додає сервери до ансамблю
-   [ZookeeperConfig::remove()](zookeeperconfig.remove.md) - Видаляє сервери з ансамблю
-   [ZookeeperException](class.zookeeperexception.md)
