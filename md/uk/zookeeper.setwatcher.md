Встановлює функцію спостерігача

-   [« Zookeeper::setLogStream](zookeeper.setlogstream.html)
    
-   [ZookeeperConfig »](class.zookeeperconfig.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Встановлює функцію спостерігача
    

# Zookeeper::setWatcher

(PECL zookeeper >= 0.1.0)

Zookeeper::setWatcher — Встановлює функцію спостерігача

### Опис

```methodsynopsis
public
   Zookeeper::setWatcher(callable $watcher_cb): bool
```

### Список параметрів

`watcher_cb`

На сервері буде встановлено спостерігач для сповіщення клієнта у разі зміни вузла.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів або їх типи неправильні або не вдається встановити спостерігача.

**Застереження**

Починаючи з версії 0.3.0, метод генерує виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::exists()](zookeeper.exists.html) - Синхронно перевіряє наявність вузла в zookeeper
-   [Zookeeper::get()](zookeeper.get.html) - Синхронно отримує дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.html)