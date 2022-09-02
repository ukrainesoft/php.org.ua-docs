---
navigation:
  - zookeeper.setwatcher.md: '« Zookeeper::setWatcher'
  - zookeeperconfig.add.md: 'ZookeeperConfig::add »'
  - index.md: PHP Manual
  - book.zookeeper.md: ZooKeeper
title: Клас ZookeeperConfig
---
# Клас ZookeeperConfig

(PECL zookeeper >= 0.6.0, ZooKeeper >= 3.5.0)

## Вступ

Клас обробки ZooKeeper Config.

## Огляд класів

```classsynopsis


     
     
      
       class ZookeeperConfig
      
      {
     

     
     /* Методы */
     
   public
   add(string $members, int $version = -1, array &$stat = null): void
public
   get(callable $watcher_cb = null, array &$stat = null): string
public
   remove(string $id_list, int $version = -1, array &$stat = null): void
public
   set(string $members, int $version = -1, array &$stat = null): void

     

    }
```

## Зміст

-   [ZookeeperConfig::add](zookeeperconfig.add.md) — Додає сервери до ансамблю
-   [ZookeeperConfig::get](zookeeperconfig.get.md) — Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключено клієнта
-   [ZookeeperConfig::remove](zookeeperconfig.remove.md) — Видаляє сервери з ансамблю
-   [ZookeeperConfig::set](zookeeperconfig.set.md) — Змінює склад ансамблю ZK та ролі його учасників
