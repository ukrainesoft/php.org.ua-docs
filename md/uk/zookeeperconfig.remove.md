---
navigation:
  - zookeeperconfig.get.md: '« ZookeeperConfig::get'
  - zookeeperconfig.set.md: 'ZookeeperConfig::set »'
  - index.md: PHP Manual
  - class.zookeeperconfig.md: ZookeeperConfig
title: 'ZookeeperConfig::remove'
---
# ZookeeperConfig::remove

(PECL zookeeper >= 0.6.0, ZooKeeper >= 3.5.0)

ZookeeperConfig::remove — Видаляє сервери з ансамблю

### Опис

```methodsynopsis
public
   ZookeeperConfig::remove(string $id_list, int $version = -1, array &$stat = null): void
```

### Список параметрів

`id_list`

Розділений комами список ідентифікаторів серверів, які потрібно видалити з ансамблю. У кожного є ідентифікатор сервера, що видаляється, тільки для основних кворумів.

`version`

Очікувана версія вузла. Функція завершиться помилкою, якщо фактична версія вузла не відповідає очікуваній версії. Якщо використовується -1, перевірка версії не виконуватиметься.

`stat`

Якщо не NULL, буде містити значення stat для шляху повернення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Метод генерує [ZookeeperException](class.zookeeperexception.md) та його похідні, коли кількість параметрів або типи неправильні або не вдається зберегти значення у вузлі.

### Приклади

**Приклад #1 Приклад використання **ZookeeperConfig::remove()****

Видалення серверів.

```php
<?php
$client = new Zookeeper();
$client->connect('localhost:2181');
$client->addAuth('digest', 'timandes:timandes');
$zkConfig = $client->getConfig();
$zkConfig->set("server.1=localhost:2888:3888:participant;0.0.0.0:2181,server.2=localhost:2889:3889:participant;0.0.0.0:2182");
$zkConfig->remove("2");
echo $zkConfig->get();
if ($r)
  echo $r;
else
  echo 'Ошибка';
?>
```

Результат виконання цього прикладу:

```
server.1=localhost:2888:3888:participant;0.0.0.0:2181
version=0xca01e881a2
```

### Дивіться також

-   [ZookeeperConfig::get()](zookeeperconfig.get.md) - Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключено клієнта
-   [ZookeeperConfig::add()](zookeeperconfig.add.md) - Додає сервери до ансамблю
-   [ZookeeperConfig::set()](zookeeperconfig.set.md) - Змінює склад ансамблю ZK та ролі його учасників
-   [ZookeeperException](class.zookeeperexception.md)
