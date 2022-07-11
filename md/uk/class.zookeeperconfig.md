- [« Zookeeper::setWatcher](zookeeper.setwatcher.md)
- [ZookeeperConfig::add »](zookeeperconfig.add.md)

- [PHP Manual](index.md)
- [ZooKeeper](book.zookeeper.md)
- Клас ZookeeperConfig

# Клас ZookeeperConfig

(PECL zookeeper \>= 0.6.0, ZooKeeper \>= 3.5.0)

## Вступ

Клас обробки ZooKeeper Config.

## Огляд класів

class **ZookeeperConfig** {

/\* Методи \*/

public [add](zookeeperconfig.add.md)(string `$members`, int `$version`
= -1, array `&$stat` = **`null`**): void

public
[get](zookeeperconfig.get.md)([callable](language.types.callable.md)
`$watcher_cb` = **`null`**, array `&$stat` = **`null`**): string

public [remove](zookeeperconfig.remove.md)(string `$id_list`, int
`$version` = -1, array `&$stat` = **`null`**): void

public [set](zookeeperconfig.set.md)(string `$members`, int `$version`
= -1, array `&$stat` = **`null`**): void

}

## Зміст

- [ZookeeperConfig::add](zookeeperconfig.add.md) — Додає сервери
в ансамбль
- [ZookeeperConfig::get](zookeeperconfig.get.md) — Синхронно
отримує останню підтверджену конфігурацію кластера ZooKeeper,
якій відомо серверу, до якого підключений клієнт
- [ZookeeperConfig::remove](zookeeperconfig.remove.md) — Видаляє
сервери з ансамблю
- [ZookeeperConfig::set](zookeeperconfig.set.md) — Змінює склад
ансамблю ZK та ролі його учасників
