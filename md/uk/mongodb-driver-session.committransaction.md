---
navigation:
  - mongodb-driver-session.advanceoperationtime.md: '« MongoDBDriverSession::advanceOperationTime'
  - mongodb-driver-session.construct.md: 'MongoDBDriverSession::construct »'
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDBDriverSession
title: 'MongoDBDriverSession::commitTransaction'
---
# MongoDBDriverSession::commitTransaction

(mongodb >=1.5.0)

MongoDBDriverSession::commitTransaction - Фіксує транзакцію

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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток [MongoDBDriverExceptionCommandException](class.mongodb-driver-exception-commandexception.md), якщо сервер не зміг зафіксувати транзакцію (наприклад, через конфлікти, проблеми з мережею). У разі, якщо виняток [MongoDBDriverExceptionCommandException::getResultDocument()](mongodb-driver-commandexception.getresultdocument.md) має елемент `"errorLabels"`, і цей масив містить значення `"TransientTransactionError"` або `"UnUnknownTransactionCommitResult"`, можна повторити спробу *всією* транзакції. У нових версіях драйвера замість цього слід використовувати [MongoDBDriverExceptionRuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md) для перевірки цієї ситуації.
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.md)якщо транзакція не може бути зафіксована (наприклад, транзакція не була запущена).

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.md) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDBDriverSession::abortTransaction()](mongodb-driver-session.aborttransaction.md) - перериває транзакцію
-   [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.md) - Запускає транзакцію
-   [MongoDBDriverExceptionRuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.md) - Повертає, чи пов'язана мітка помилки з винятком
