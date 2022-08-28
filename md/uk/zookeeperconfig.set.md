Змінює склад ансамблю ZK та ролі його учасників

-   [« ZookeeperConfig::remove](zookeeperconfig.remove.html)
    
-   [ZookeeperException »](class.zookeeperexception.html)
    
-   [PHP Manual](index.html)
    
-   [ZookeeperConfig](class.zookeeperconfig.html)
    
-   Змінює склад ансамблю ZK та ролі його учасників
    

# ZookeeperConfig::set

(PECL zookeeper >= 0.6.0, ZooKeeper >= 3.5.0)

ZookeeperConfig::set — Змінює склад ансамблю ZK та ролі його учасників

### Опис

```methodsynopsis
public
   ZookeeperConfig::set(string $members, int $version = -1, array &$stat = null): void
```

### Список параметрів

`members`

Розділений комами список нових членів ансамблю (наприклад, вміст конфігураційного файлу) - для використання тільки з неінкрементною реконфігурацією.

`version`

Очікувана версія вузла. Функція завершиться помилкою, якщо фактична версія вузла не відповідає очікуваній версії. Якщо використовується -1, перевірка версії не виконуватиметься.

`stat`

Якщо не NULL, буде містити значення stat для шляху повернення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Метод генерує [ZookeeperException](class.zookeeperexception.html) та його похідні, коли кількість параметрів або типи неправильні або не вдається зберегти значення у вузлі.

### Приклади

**Приклад #1 Приклад використання **ZookeeperConfig::set()****

Реконфігурація

```php
<?php
$client = new Zookeeper();
$client->connect('localhost:2181');
$client->addAuth('digest', 'timandes:timandes');
$zkConfig = $client->getConfig();
$zkConfig->set("server.1=localhost:2888:3888:participant;0.0.0.0:2181");
?>
```

### Дивіться також

-   [ZookeeperConfig::get()](zookeeperconfig.get.html) - Синхронно отримує останню підтверджену конфігурацію кластера ZooKeeper, про яку відомо серверу, до якого підключено клієнта
-   [ZookeeperConfig::add()](zookeeperconfig.add.html) - Додає сервери до ансамблю
-   [ZookeeperConfig::remove()](zookeeperconfig.remove.html) - Видаляє сервери з ансамблю
-   [ZookeeperException](class.zookeeperexception.html)