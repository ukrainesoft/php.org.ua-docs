---
navigation:
  - zookeeper.getconfig.md: '« Zookeeper::getConfig'
  - zookeeper.getstate.md: 'Zookeeper::getState »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::getRecvTimeout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::getRecvTimeout

(PECL zookeeper >= 0.1.0)

Zookeeper::getRecvTimeout — Повертає час очікування для сесії, дійсний, тільки якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOO\_CONNECTED\_STATE). Це значення може змінитися після повторного підключення до сервера

### Опис

```methodsynopsis
public
   Zookeeper::getRecvTimeout(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час очікування для сесії у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP у разі збою операції.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.md)
