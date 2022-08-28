Запускає транзакцію

-   [« MongoDB\\Driver\\Session::isInTransaction](mongodb-driver-session.isintransaction.html)
    
-   [MongoDB\\Driver\\ClientEncryption »](class.mongodb-driver-clientencryption.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html)
    
-   Запускає транзакцію
    

# MongoDBDriverSession::startTransaction

(mongodb >=1.5.0)

MongoDBDriverSession::startTransaction — Запускає транзакцію

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::startTransaction(?array $options = null): void
```

Запускає багатодокументну транзакцію, пов'язану із сеансом. У будь-який час ви можете мати не більше однієї відкритої транзакції для сеансу. Після запуску транзакції об'єкт сеансу має бути переданий кожній операції за допомогою опції `"session"` (наприклад, [MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.html)), щоб пов'язати цю операцію з транзакцією.

Транзакції можуть бути зафіксовані через [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.html) та перервані за допомогою [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.html). Транзакції також автоматично перериваються, коли сеанс закривається зі складання сміття або явно викликається. [MongoDB\\Driver\\Session::endSession()](mongodb-driver-session.endsession.html)

### Список параметрів

`options`

Параметри можуть бути передані як аргумент цим методом. Кожен елемент у цьому масиві опцій перевизначає відповідну опцію з опції `"defaultTransactionOptions"`, якщо вона встановлена ​​під час запуску сеансу з [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html)

**options**

| Опция | Тип | Описание |
| --- | --- | --- |
| maxCommitTimeMS | integer |  |
| Максимальний період часу в мілісекундах, протягом якого може виконуватись одна команда `commitTransaction` |  |  |

Якщо зазначено, `maxCommitTimeMS` має бути 32-розрядним цілим числом зі знаком, великим або рівним нулю.

| | readConcern | [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html)

Гарантія для застосування до операції.

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference | [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | writeConcern | [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html)

Гарантія запису для застосування до операції.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html)
-   Видає виняток [MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.html), якщо транзакція не може бути запущена через проблему на стороні сервера (наприклад, не вдалося отримати блокування).
-   Видає виняток [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html)якщо транзакція не може бути запущена (наприклад, транзакція вже була запущена).

### список змін

| Версия | Описание |
| --- | --- |
| PECL mongodb 1.6.0 |  |
| Доданий параметр `"maxCommitTimeMS"` |  |

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.html) - Запуск нового клієнтського сеансу для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.html) - Фіксує транзакцію
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.html) - перериває транзакцію