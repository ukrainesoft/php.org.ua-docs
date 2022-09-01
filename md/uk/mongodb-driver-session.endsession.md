---
navigation:
  - mongodb-driver-session.construct.html: '« MongoDBDriverSession::construct'
  - mongodb-driver-session.getclustertime.html: 'MongoDBDriverSession::getClusterTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::endSession'
---
# MongoDBDriverSession::endSession

(mongodb >=1.5.0)

MongoDBDriverSession::endSession — Завершує сеанс

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.html) - Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDBDriverSession::abortTransaction()](mongodb-driver-session.aborttransaction.html) - перериває транзакцію
-   [MongoDBDriverSession::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію
