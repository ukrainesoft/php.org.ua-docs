---
navigation:
  - zookeeper.getconfig.html: '« Zookeeper::getConfig'
  - zookeeper.getstate.html: 'Zookeeper::getState »'
  - index.html: PHP Manual
  - class.zookeeper.html: Zookeeper
title: 'Zookeeper::getRecvTimeout'
---
# Zookeeper::getRecvTimeout

(PECL zookeeper >= 0.1.0)

Zookeeper::getRecvTimeout — Повертає час очікування для сесії, дійсний, тільки якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE). Це значення може змінитися після повторного підключення до сервера

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

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.html)
