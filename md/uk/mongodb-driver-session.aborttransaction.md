---
navigation:
  - class.mongodb-driver-session.md: « MongoDB\\Driver\\Session
  - mongodb-driver-session.advanceclustertime.md: 'MongoDB\\Driver\\Session::advanceClusterTime »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::abortTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::abortTransaction

(mongodb >=1.5.0)

MongoDB\\Driver\\Session::abortTransaction — Перериває транзакцію

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

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md), якщо транзакція не може бути перервана (наприклад, транзакцію не було розпочато).

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) \- Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.md) \- Фіксує транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.md) \- Запускає транзакцію
