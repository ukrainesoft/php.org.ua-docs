Перевіряє, чи можна відновити поточний стан підключення ZooKeeper

-   [« Zookeeper::getState](zookeeper.getstate.html)
    
-   [Zookeeper::set »](zookeeper.set.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Перевіряє, чи можна відновити поточний стан підключення ZooKeeper
    

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

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getClientId()](zookeeper.getclientid.html) - Повертає ідентифікатор сесії клієнта, дійсний тільки в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)
-   [Стан ZooKeeper](class.zookeeper.html#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.html)