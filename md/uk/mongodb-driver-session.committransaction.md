---
navigation:
  - mongodb-driver-session.advanceoperationtime.html: '« MongoDBDriverSession::advanceOperationTime'
  - mongodb-driver-session.construct.html: 'MongoDBDriverSession::construct »'
  - index.html: PHP Manual
  - class.mongodb-driver-session.html: MongoDBDriverSession
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

-   При помилці парсингу аргумент кидає виняток [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDBDriverExceptionCommandException](class.mongodb-driver-exception-commandexception.html), якщо сервер не зміг зафіксувати транзакцію (наприклад, через конфлікти, проблеми з мережею). У разі, якщо виняток [MongoDBDriverExceptionCommandException::getResultDocument()](mongodb-driver-commandexception.getresultdocument.html) має елемент `"errorLabels"`, і цей масив містить значення `"TransientTransactionError"` або `"UnUnknownTransactionCommitResult"`, можна повторити спробу *всією* транзакції. У нових версіях драйвера замість цього слід використовувати [MongoDBDriverExceptionRuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.html) для перевірки цієї ситуації.
-   Видає виняток [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html)якщо транзакція не може бути зафіксована (наприклад, транзакція не була запущена).

### Дивіться також

-   [MongoDBDriverManager::startSession()](mongodb-driver-manager.startsession.html) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDBDriverSession::abortTransaction()](mongodb-driver-session.aborttransaction.html) - перериває транзакцію
-   [MongoDBDriverSession::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію
-   [MongoDBDriverExceptionRuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.html) - Повертає, чи пов'язана мітка помилки з винятком
