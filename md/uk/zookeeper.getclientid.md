Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)

-   [« Zookeeper::getChildren](zookeeper.getchildren.html)
    
-   [Zookeeper::getConfig »](zookeeper.getconfig.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)
    

# Zookeeper::getClientId

(PECL zookeeper >= 0.1.0)

Zookeeper::getClientId — Повертає ідентифікатор сесії клієнта, дійсний лише в тому випадку, якщо підключення в даний час підключено (тобто останній стан спостерігача - ZOOCONNECTEDSTATE)

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

Починаючи з версії 0.3.0 метод викидає [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::construct()](zookeeper.construct.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [Zookeeper::getState()](zookeeper.getstate.html) - Отримує стан з'єднання zookeeper
-   [Стан ZooKeeper](class.zookeeper.html#zookeeper.class.constants.states)
-   [ZookeeperException](class.zookeeperexception.html)