---
navigation:
  - mongodb-driver-session.construct.md: '« MongoDB\\Driver\\Session::\_\_construct'
  - mongodb-driver-session.getclustertime.md: 'MongoDB\\Driver\\Session::getClusterTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::endSession'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::endSession

(mongodb >=1.5.0)

MongoDB\\Driver\\Session::endSession — Завершує сеанс

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::endSession(): void
```

Цей метод закриває існуючий сеанс. Якщо транзакція була пов'язана з цим сеансом, транзакція буде перервана. Після виклику цього методу програми не повинні викликати інші методи у сеансі.

> **Зауваження**: Сесії також закриті під час збору сміття Не повинно бути потреби викликати цей метод за нормальних обставин.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) \- Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.md) \- перериває транзакцію
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.md) \- Фіксує транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.md) \- Запускає транзакцію
