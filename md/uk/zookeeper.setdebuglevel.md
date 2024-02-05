---
navigation:
  - zookeeper.setacl.md: '« Zookeeper::setAcl'
  - zookeeper.setdeterministicconnorder.md: 'Zookeeper::setDeterministicConnOrder »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::setDebugLevel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів або типи неправильні або не вдається встановити рівень логування.

**Застереження**

Починаючи з версії 0.3.0 цей метод генерує виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Приклади

**Пример #1 Пример использования**Zookeeper::setDebugLevel()\*\*\*\*

Встановлення рівня логування

```php
<?php
$r = Zookeeper::setDebugLevel(Zookeeper::LOG_LEVEL_WARN);
if ($r)
  echo 'Успешно';
else
  echo 'Ошибка';
?>
?>
```

Результат виконання наведеного прикладу:

```
SUCCESS
```

### Дивіться також

-   [Рівень логування ZooKeeper](class.zookeeper.md#zookeeper.class.constants.log-levels)
-   [ZookeeperException](class.zookeeperexception.md)
