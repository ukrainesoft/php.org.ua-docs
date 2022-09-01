---
navigation:
  - class.mongodb-driver-session.html: « MongoDBDriverSession
  - mongodb-driver-session.advanceclustertime.html: 'MongoDBDriverSession::advanceClusterTime »'
  - index.html: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
title: 'MongoDBDriverSession::abortTransaction'
---
# MongoDBDriverSession::abortTransaction

(mongodb >=1.5.0)

MongoDBDriverSession::abortTransaction — Перериває транзакцію

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::abortTransaction(): void
```

Завершує багатодокументну транзакцію та відкочує будь-які зміни даних, зроблені операціями усередині транзакції. Тобто транзакція закінчується без збереження будь-яких змін, внесених операціями до транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html), якщо транзакція може бути перервана (наприклад, транзакція розпочато).

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.html) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDBDriverSession::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію
