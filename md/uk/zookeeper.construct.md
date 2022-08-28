Створює дескриптор для спілкування з zookeeper

-   [« Zookeeper::connect](zookeeper.connect.html)
    
-   [Zookeeper::create »](zookeeper.create.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Створює дескриптор для спілкування з zookeeper
    

# Zookeeper::construct

(PECL zookeeper >= 0.1.0)

Zookeeper::construct — Створює дескриптор для спілкування з zookeeper

### Опис

public **Zookeeper::construct**(string `$host` [callable](language.types.callable.html) `$watcher_cb` **`null`**, int `$recv_timeout`

Метод створює новий дескриптор та сеанс zookeeper, який відповідає цьому дескриптору. Встановлення сеансу асинхронне, тому сеанс не слід вважати встановленим доти, доки не буде отримано подію стану ZOOCONNECTEDSTATE.

### Список параметрів

`host`

Розділені комами пари host:port, кожна з яких відповідає zk-серверу. Наприклад, "127.0.0.1:3000,127.0.0.1:3001,127.0.0.1:3002"

`watcher_cb`

Callback – функція глобального спостерігача. Коли ініціюються повідомлення, ця функція буде викликана.

`recv_timeout`

Час очікування для сеансу, дійсний тільки якщо підключення в даний момент підключені (тобто стан останнього спостерігача ZOOCONNECTEDSTATE).

### Помилки

Метод видає PHP повідомлення про помилку/попередження, коли кількість параметрів або їх типи неправильні або не вдалося ініціалізувати екземпляр.

**Застереження**

Починаючи з версії 0.3.0, метод викидає виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::connect()](zookeeper.connect.html) - Створює дескриптор для спілкування з zookeeper
-   [ZookeeperException](class.zookeeperexception.html)