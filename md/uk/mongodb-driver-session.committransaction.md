---
navigation:
  - mongodb-driver-session.advanceoperationtime.md: '« MongoDB\\Driver\\Session::advanceOperationTime'
  - mongodb-driver-session.construct.md: 'MongoDB\\Driver\\Session::\_\_construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::commitTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::commitTransaction

(mongodb >=1.5.0)

MongoDB\\Driver\\Session::commitTransaction - Фіксує транзакцію

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::commitTransaction(): void
```

Зберігає зміни, внесені операціями до багатодокументної транзакції та завершує транзакцію. До фіксації жодна зміна даних, зроблених з транзакції, буде видно поза транзакції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.md), якщо сервер не зміг зафіксувати транзакцію (наприклад, через конфлікти, проблеми з мережею). У разі, якщо виняток[MongoDB\\Driver\\Exception\\CommandException::getResultDocument()](mongodb-driver-commandexception.getresultdocument.md)має елемент`"errorLabels"`, і цей масив містить значення`"TransientTransactionError"`или`"UnUnknownTransactionCommitResult"`, можна повторити спробу*всією*транзакції. У нових версіях драйвера замість цього слід використовувати[MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md)для перевірки цієї ситуації.
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md), якщо транзакція не може бути зафіксована (наприклад, транзакція не була запущена).

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) \- Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.md) \- перериває транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.md) \- Запускає транзакцію
-   [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md) \- Повертає, чи пов'язана мітка помилки з винятком
