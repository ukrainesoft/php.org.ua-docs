---
navigation:
  - zookeeper.addauth.md: '« Zookeeper::addAuth'
  - zookeeper.connect.md: 'Zookeeper::connect »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::close

(PECL zookeeper >= 0.5.0)

Zookeeper::close — Закриває обробник zookeeper та звільняє будь-які ресурси

### Опис

```methodsynopsis
public
   Zookeeper::close(): void
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Метод генерирует[ZookeeperException](class.zookeeperexception.md) та його похідні при закритті неініціалізованого екземпляра.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.md)
