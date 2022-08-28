Встановлює потік, який використовуватиметься бібліотекою для логування

-   [« Zookeeper::setDeterministicConnOrder](zookeeper.setdeterministicconnorder.html)
    
-   [Zookeeper::setWatcher »](zookeeper.setwatcher.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Встановлює потік, який використовуватиметься бібліотекою для логування
    

# Zookeeper::setLogStream

(PECL zookeeper >= 0.1.0)

Zookeeper::setLogStream — Встановлює потік, який використовуватиметься бібліотекою для логування

### Опис

```methodsynopsis
public
   Zookeeper::setLogStream(resource $stream): bool
```

Бібліотека zookeeper використовує stderr як поток логування за замовчуванням. Програма повинна переконатися, що потік доступний для запису. Передача в NULL скидає потік до значення за промовчанням (stderr).

### Список параметрів

`stream`

Потік, який використовуватиметься бібліотекою для логування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів чи типи неправильні або операція завершується невдало.

**Застереження**

Починаючи з версії 0.3.0, метод генерує виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Дивіться також

-   [Zookeeper::setDebugLevel()](zookeeper.setdebuglevel.html) - Встановлює рівень логування для бібліотеки
-   [ZookeeperException](class.zookeeperexception.html)