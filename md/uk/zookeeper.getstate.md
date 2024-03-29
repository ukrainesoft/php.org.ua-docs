---
navigation:
  - zookeeper.getrecvtimeout.md: '« Zookeeper::getRecvTimeout'
  - zookeeper.isrecoverable.md: 'Zookeeper::isRecoverable »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::getState'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::getState

(PECL zookeeper >= 0.1.0)

Zookeeper::getState — Отримує стан з'єднання zookeeper

### Опис

```methodsynopsis
public
   Zookeeper::getState(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає стан з'єднання zookeeper у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає PHP повідомлення про помилку/попередження, коли йому не вдається отримати стан з'єднання zookeeper.

**Застереження**

Починаючи з версії 0.3.0 цей метод генерує виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getClientId()](zookeeper.getclientid.md) \- Повертає ідентифікатор сесії клієнта, дійсний тільки в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOO\_CONNECTED\_STATE)
-   [Стан ZooKeeper](class.zookeeper.md#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.md)
