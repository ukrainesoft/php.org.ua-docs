---
navigation:
  - class.zookeeperconfig.md: « ZookeeperConfig
  - zookeeperconfig.get.md: 'ZookeeperConfig::get »'
  - index.md: PHP Manual
  - class.zookeeperconfig.md: ZookeeperConfig
title: 'ZookeeperConfig::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZookeeperConfig::add

(PECL zookeeper >= 0.6.0, ZooKeeper >= 3.5.0)

ZookeeperConfig::add — Додає сервери до ансамблю

### Опис

```methodsynopsis
public
   ZookeeperConfig::add(string $members, int $version = -1, array &$stat = null): void
```

### Список параметрів

`members`

Розділений комами список серверів для додавання до ансамблю. Кожен з них має рядок конфігурації для сервера, що додається (як показано у файлі конфігурації), тільки для основних кворумів.

`version`

Очікувана версія вузла. Функція завершиться помилкою, якщо фактична версія вузла не відповідає очікуваній версії. Якщо використовується -1, перевірка версії не виконуватиметься.

`stat`

Якщо не NULL, буде містити значення stat для шляху повернення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Метод генерирует[ZookeeperException](class.zookeeperexception.md) та його похідні, коли кількість параметрів або типи неправильні або не вдається зберегти значення у вузлі.

### Приклади

**Приклад #1 Приклад використання** ZookeeperConfig::add()\*\*\*\*

Додавання серверів.

```php
<?php
$client = new Zookeeper();
$client->connect('localhost:2181');
$client->addAuth('digest', 'timandes:timandes');
$zkConfig = $client->getConfig();
$zkConfig->set("server.1=localhost:2888:3888:participant;0.0.0.0:2181");
$zkConfig->add("server.2=localhost:2889:3889:participant;0.0.0.0:2182");
$r = $zkConfig->get();
if ($r)
  echo $r;
else
  echo 'Ошибка';
?>
```

Результат виконання наведеного прикладу:

```
server.1=localhost:2888:3888:participant;0.0.0.0:2181
server.2=localhost:2889:3889:participant;0.0.0.0:2182
version=0xca01e881a2
```

### Дивіться також

-   [ZookeeperConfig::get()](zookeeperconfig.get.md) \- Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключено клієнта
-   [ZookeeperConfig::set()](zookeeperconfig.set.md) \- Змінює склад ансамблю ZK та ролі його учасників
-   [ZookeeperConfig::remove()](zookeeperconfig.remove.md) \- Видаляє сервери з ансамблю
-   [ZookeeperException](class.zookeeperexception.md)
