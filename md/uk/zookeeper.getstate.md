Отримує стан з'єднання zookeeper

-   [« Zookeeper::getRecvTimeout](zookeeper.getrecvtimeout.html)
    
-   [Zookeeper::isRecoverable »](zookeeper.isrecoverable.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Отримує стан з'єднання zookeeper
    

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

Починаючи з версії 0.3.0 цей метод генерує виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::\_\_construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getClientId()](zookeeper.getclientid.html) - Повертає ідентифікатор сесії клієнта, дійсний тільки в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)
-   [Состояния ZooKeeper](class.zookeeper.html#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.html)