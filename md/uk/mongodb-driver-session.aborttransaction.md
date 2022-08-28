Перериває транзакцію

-   [« MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   [MongoDB\\Driver\\Session::advanceClusterTime »](mongodb-driver-session.advanceclustertime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Перериває транзакцію
    

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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html), якщо транзакція може бути перервана (наприклад, транзакція розпочато).

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію