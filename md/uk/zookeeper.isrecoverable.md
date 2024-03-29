---
navigation:
  - zookeeper.getstate.md: '« Zookeeper::getState'
  - zookeeper.set.md: 'Zookeeper::set »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::isRecoverable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Zookeeper::isRecoverable

(PECL zookeeper >= 0.1.0)

Zookeeper::isRecoverable — Перевіряє, чи можна відновити поточний стан підключення ZooKeeper

### Опис

```methodsynopsis
public
   Zookeeper::isRecoverable(): bool
```

Програма має закрити дескриптор і спробувати перепідключитися.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає true/false у разі успішного виконання та false у разі виникнення помилки.

### Помилки

Метод видає помилку/попередження PHP у разі збою операції.

**Застереження**

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.md) \- Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getClientId()](zookeeper.getclientid.md) \- Повертає ідентифікатор сесії клієнта, дійсний тільки в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOO\_CONNECTED\_STATE)
-   [Стан ZooKeeper](class.zookeeper.md#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.md)
