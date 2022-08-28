Встановлює рівень логування для бібліотеки

-   [« Zookeeper::setAcl](zookeeper.setacl.html)
    
-   [Zookeeper::setDeterministicConnOrder »](zookeeper.setdeterministicconnorder.html)
    
-   [PHP Manual](index.html)
    
-   [Zookeeper](class.zookeeper.html)
    
-   Встановлює рівень логування для бібліотеки
    

# Zookeeper::setDebugLevel

(PECL zookeeper >= 0.1.0)

Zookeeper::setDebugLevel — Встановлює рівень логування для бібліотеки

### Опис

```methodsynopsis
public
   static
   Zookeeper::setDebugLevel(int $logLevel): bool
```

### Список параметрів

`logLevel`

Константи рівня логування ZooKeeper.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів або типи неправильні або не вдається встановити рівень логування.

**Застереження**

Починаючи з версії 0.3.0, цей метод генерує виняток [ZookeeperException](class.zookeeperexception.html) та його похідні.

### Приклади

**Приклад #1 Приклад використання **Zookeeper::setDebugLevel()****

Встановлення рівня логування

```php
<?php
$r = Zookeeper::setDebugLevel(Zookeeper::LOG_LEVEL_WARN);
if ($r)
  echo 'Успешно';
else
  echo 'Ошибка';
?>
?>
```

Результат виконання цього прикладу:

```
SUCCESS
```

### Дивіться також

-   [Уровень логирования ZooKeeper](class.zookeeper.html#zookeeper.class.constants.log-levels)
-   [ZookeeperException](class.zookeeperexception.html)