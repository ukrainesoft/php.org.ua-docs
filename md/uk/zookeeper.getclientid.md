---
navigation:
  - zookeeper.getchildren.md: '« Zookeeper::getChildren'
  - zookeeper.getconfig.md: 'Zookeeper::getConfig »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::getClientId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::getClientId

(PECL zookeeper >= 0.1.0)

Zookeeper::getClientId — Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOO\_CONNECTED\_STATE)

### Опис

```methodsynopsis
public
   Zookeeper::getClientId(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ідентифікатор клієнтської сесії у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP, коли не може отримати ідентифікатор сеансу клієнта.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getState()](zookeeper.getstate.md) \- Отримує стан з'єднання zookeeper
-   [Стан ZooKeeper](class.zookeeper.md#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.md)
