---
navigation:
  - zookeeper.setdeterministicconnorder.md: '« Zookeeper::setDeterministicConnOrder'
  - zookeeper.setwatcher.md: 'Zookeeper::setWatcher »'
  - index.md: PHP Manual
  - class.zookeeper.md: Zookeeper
title: 'Zookeeper::setLogStream'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Метод видає PHP-повідомлення про помилку/попередження, коли кількість параметрів чи типи неправильні або операція завершується невдало.

**Застереження**

Починаючи з версії 0.3.0, метод генерує виняток [ZookeeperException](class.zookeeperexception.md) та його похідні.

### Дивіться також

-   [Zookeeper::setDebugLevel()](zookeeper.setdebuglevel.md) \- Встановлює рівень логування для бібліотеки
-   [ZookeeperException](class.zookeeperexception.md)
