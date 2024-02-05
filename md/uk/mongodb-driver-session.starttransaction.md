---
navigation:
  - mongodb-driver-session.isintransaction.md: '« MongoDB\\Driver\\Session::isInTransaction'
  - class.mongodb-driver-clientencryption.md: MongoDB\\Driver\\ClientEncryption »
  - index.md: PHP Manual
  - class.mongodb-driver-session.md: MongoDB\\Driver\\Session
title: 'MongoDB\\Driver\\Session::startTransaction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# MongoDB\\Driver\\Session::startTransaction

(mongodb >=1.5.0)

MongoDB\\Driver\\Session::startTransaction — Запускає транзакцію

### Опис

```methodsynopsis
final public MongoDB\Driver\Session::startTransaction(?array $options = null): void
```

Запускає багатодокументну транзакцію, пов'язану із сеансом. У будь-який час ви можете мати не більше однієї відкритої транзакції для сеансу. Після запуску транзакції об'єкт сеансу має бути переданий кожній операції за допомогою опції `"session"`(например,[MongoDB\\Driver\\Manager::executeBulkWrite()](mongodb-driver-manager.executebulkwrite.md)), щоб пов'язати цю операцію з транзакцією.

Транзакції можуть бути зафіксовані через [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.md) та перервані за допомогою [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.md). Транзакції також автоматично перериваються, коли сеанс закривається зі складання сміття або явно викликається. [MongoDB\\Driver\\Session::endSession()](mongodb-driver-session.endsession.md)

### Список параметрів

`options`

Параметри можуть бути передані як аргумент цим методом. Кожен елемент у цьому масиві опцій перевизначає відповідну опцію з опції `"defaultTransactionOptions"`, если она установлена при запуске сеанса с[MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md)

**options**

| Опция | Тип | Опис |
| --- | --- | --- |
| maxCommitTimeMS | integer |  |
| Максимальний період часу в мілісекундах, протягом якого може виконуватись одна команда `commitTransaction` |  |  |

Якщо зазначено, `maxCommitTimeMS` має бути 32-розрядним цілим числом зі знаком, великим або рівним нулю.

| | readConcern |[MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.md)

Гарантія для застосування до операції.

Ця опція доступна в MongoDB 3.2+ і призведе до виключення під час виконання, якщо вказана для старої версії сервера.

| | readPreference |[MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.md)

Перевага читання, що використовується для вибору сервера для виконання операції.

| | writeConcern |[MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.md)

Гарантія запису для застосування до операції.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   При помилці парсингу аргумент кидає виняток[MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md)
-   Видає виняток[MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.md), якщо транзакція не може бути запущена через проблему на стороні сервера (наприклад, не вдалося отримати блокування).
-   Видає виняток[MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.md)якщо транзакція не може бути запущена (наприклад, транзакція вже була запущена).

### список змін

| Версия | Опис |
| --- | --- |
| PECL mongodb 1.6.0 |  |
| Добавлен параметр`"maxCommitTimeMS"` |  |

### Дивіться також

-   [MongoDB\\Driver\\Manager::startSession()](mongodb-driver-manager.startsession.md) \- Запускає новий сеанс клієнта для використання з цим клієнтом
-   [MongoDB\\Driver\\Session::commitTransaction()](mongodb-driver-session.committransaction.md) \- Фіксує транзакцію
-   [MongoDB\\Driver\\Session::abortTransaction()](mongodb-driver-session.aborttransaction.md) \- перериває транзакцію
