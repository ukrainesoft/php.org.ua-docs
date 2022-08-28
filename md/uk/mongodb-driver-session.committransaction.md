Фіксує транзакцію

-   [« MongoDB\\Driver\\Session::advanceOperationTime](mongodb-driver-session.advanceoperationtime.html)
    
-   [MongoDB\\Driver\\Session::\_\_construct »](mongodb-driver-session.construct.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Фіксує транзакцію
    

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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.html), якщо сервер не зміг зафіксувати транзакцію (наприклад, через конфлікти, проблеми з мережею). У разі, якщо виняток [MongoDB\\Driver\\Exception\\CommandException::getResultDocument()](mongodb-driver-commandexception.getresultdocument.html) має елемент `"errorLabels"`, і цей масив містить значення `"TransientTransactionError"` або `"UnUnknownTransactionCommitResult"`, можна повторити спробу *всією* транзакції. У нових версіях драйвера замість цього слід використовувати [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.html) для перевірки цієї ситуації.
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html)якщо транзакція не може бути зафіксована (наприклад, транзакція не була запущена).

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.html) - перериває транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію
-   [MongoDB\\Driver\\Exception\\RuntimeException::hasErrorLabel()](mongodb-driver-runtimeexception.haserrorlabel.html) - Повертає, чи пов'язана мітка помилки з винятком