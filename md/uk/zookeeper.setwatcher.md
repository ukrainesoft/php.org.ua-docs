---
navigation:
  - zookeeper.setlogstream.md: '« Zookeeper::setLogStream'
  - class.zookeeperconfig.md: ZookeeperConfig »
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::setWatcher'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів або їх типи неправильні або не вдається встановити спостерігача.

**Застереження**

Починаючи з версії 0.3.0, метод генерує виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::exists()](zookeeper.exists.md) \- Синхронно перевіряє наявність вузла в zookeeper
-   [Zookeeper::get()](zookeeper.get.md) \- Синхронно отримує дані, пов'язані з вузлом
-   [ZookeeperException](class.zookeeperexception.md)
