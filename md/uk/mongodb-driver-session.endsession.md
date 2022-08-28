Завершує сеанс

-   [« MongoDB\\Driver\\Session::\_\_construct](mongodb-driver-session.construct.html)
    
-   [MongoDB\\Driver\\Session::getClusterTime »](mongodb-driver-session.getclustertime.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Завершує сеанс
    

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

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html) - Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.html) - перериває транзакцію
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDB\\Driver\\Session::startTransaction()](mongodb-driver-session.starttransaction.html) - Запускає транзакцію