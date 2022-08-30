Драйвер MongoDB

-   [« db2tables](function.db2-tables.html)
    
-   [Установка и настройка »](mongodb.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Модулі для роботи з базами даних окремих виробників](refs.database.vendors.html)
    
-   Драйвер MongoDB
    

# Драйвер MongoDB

Цей модуль розроблено на основі бібліотек [» libmongoc](https://github.com/mongodb/mongo-c-driver) і [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson). Він надає мінімальне API для ключового функціоналу драйвера: [команды](class.mongodb-driver-command.html) [запити](class.mongodb-driver-query.html) [записи](class.mongodb-driver-bulkwrite.html) [управление соединением](class.mongodb-driver-manager.html) і [сериализация BSON](book.bson.html)

Саморобні бібліотеки PHP, що вимагають цей модуль, можуть надавати високорівневі API, такі як: збирачі запитів, методи-помічники для індивідуальних команд та GridFS. Розробники додатків повинні розглянути питання щодо використання цього модуля спільно з [» библиотекой MongoDB PHP](https://github.com/mongodb/mongo-php-library), яка реалізує такі ж високорівневі драйвери API MongoDB, як і для інших мов. Подібний поділ завдань дозволяє цьому драйверу сконцентруватися на головних завданнях, що стоять перед ним – підвищення продуктивності.

-   [Установка и настройка](mongodb.setup.html)
    -   [Требования](mongodb.requirements.html)
    -   [Установка](mongodb.installation.html)
    -   [Настройка во время выполнения](mongodb.configuration.html)
    -   [Предопределённые константы](mongodb.constants.html)
-   [Навчальні матеріали](mongodb.tutorial.html)
    -   [Использование библиотеки PHP для MongoDB (PHPLIB)](mongodb.tutorial.library.html)
    -   [Моніторинг продуктивності програми (Application Performance Monitoring або APM)](mongodb.tutorial.apm.html)
-   [Архитектура и внутреннее устройство драйвера](mongodb.architecture.html) — Огляд архітектури драйвера та її особливостей
    -   [Архитектура](mongodb.overview.html) - Огляд архітектури
    -   [Соединения](mongodb.connection-handling.html) — Обробка з'єднання та сталість
    -   [Постійні дані](mongodb.persistence.html) — Серіалізація та десеріалізація змінних PHP у MongoDB
-   [Безпека](mongodb.security.html)
    -   [Атака с помощью инъекций в запросе](mongodb.security.request_injection.html)
    -   [Атака с помощью инъекций в скриптах](mongodb.security.script_injection.html)
-   [MongoDBDriver](book.mongodb.html) - Класи драйвера MongoDB
    -   [MongoDBDriverManager](class.mongodb-driver-manager.html) - Клас MongoDBDriverManager
    -   [MongoDBDriverCommand](class.mongodb-driver-command.html) - Клас The MongoDBDriverCommand
    -   [MongoDBDriverQuery](class.mongodb-driver-query.html) - Клас MongoDBDriverQuery
    -   [MongoDBDriverBulkWrite](class.mongodb-driver-bulkwrite.html) - Клас MongoDBDriverBulkWrite
    -   [MongoDBDriverSession](class.mongodb-driver-session.html) - Клас MongoDBDriverSession
    -   [MongoDBDriverClientEncryption](class.mongodb-driver-clientencryption.html) - Клас MongoDBDriverClientEncryption
    -   [MongoDBDriverServerApi](class.mongodb-driver-serverapi.html) - Клас MongoDBDriverServerApi
    -   [MongoDBDriverWriteConcern](class.mongodb-driver-writeconcern.html) - Клас MongoDBDriverWriteConcern
    -   [MongoDBDriverReadPreference](class.mongodb-driver-readpreference.html) - Клас MongoDBDriverReadPreference
    -   [MongoDBDriverReadConcern](class.mongodb-driver-readconcern.html) - Клас MongoDBDriverReadConcern
    -   [MongoDBDriverCursor](class.mongodb-driver-cursor.html) - Клас MongoDBDriverCursor
    -   [MongoDBDriverCursorId](class.mongodb-driver-cursorid.html) - Клас MongoDBDriverCursorId
    -   [MongoDBDriverCursorInterface](class.mongodb-driver-cursorinterface.html) - Інтерфейс MongoDBDriverCursorInterface
    -   [MongoDBDriverServer](class.mongodb-driver-server.html) - Клас MongoDBDriverServer
    -   [MongoDBDriverServerDescription](class.mongodb-driver-serverdescription.html) - Клас MongoDBDriverServerDescription
    -   [MongoDBDriverTopologyDescription](class.mongodb-driver-topologydescription.html) - Клас MongoDBDriverTopologyDescription
    -   [MongoDBDriverWriteConcernError](class.mongodb-driver-writeconcernerror.html) - Клас The MongoDBDriverWriteConcernError
    -   [MongoDBDriverWriteError](class.mongodb-driver-writeerror.html) - Клас MongoDBDriverWriteError
    -   [MongoDBDriverWriteResult](class.mongodb-driver-writeresult.html) - Клас MongoDBDriverWriteResult
-   [MongoDBBSON](book.bson.html) — Класи типів BSON та функції серіалізації
    -   [Функції](ref.bson.functions.html)
    -   [MongoDBBSONBinary](class.mongodb-bson-binary.html) - Клас MongoDBBSONBinary
    -   [MongoDBBSONDecimal128](class.mongodb-bson-decimal128.html) - Клас MongoDBBSONDecimal128
    -   [MongoDBBSONJavascript](class.mongodb-bson-javascript.html) - Клас MongoDBBSONJavascript
    -   [MongoDBBSONMaxKey](class.mongodb-bson-maxkey.html) - Клас MongoDBBSONMaxKey
    -   [MongoDBBSONMinKey](class.mongodb-bson-minkey.html) - Клас MongoDBBSONMinKey
    -   [MongoDBBSONObjectId](class.mongodb-bson-objectid.html) - Клас MongoDBBSONObjectId
    -   [MongoDBBSONRegex](class.mongodb-bson-regex.html) - Клас MongoDBBSONRegex
    -   [MongoDBBSONTimestamp](class.mongodb-bson-timestamp.html) - Клас MongoDBBSONTimestamp
    -   [MongoDBBSONUTCDateTime](class.mongodb-bson-utcdatetime.html) - Клас MongoDBBSONUTCDateTime
    -   [MongoDBBSONType](class.mongodb-bson-type.html) - Інтерфейс MongoDBBSONType
    -   [MongoDBBSONPersistable](class.mongodb-bson-persistable.html) - Інтерфейс MongoDBBSONPersistable
    -   [MongoDBBSONSerializable](class.mongodb-bson-serializable.html) - Інтерфейс MongoDBBSONSerializable
    -   [MongoDBBSONUnserializable](class.mongodb-bson-unserializable.html) - Інтерфейс MongoDBBSONUnserializable
    -   [MongoDBBSONBinaryInterface](class.mongodb-bson-binaryinterface.html) - Інтерфейс MongoDBBSONBinaryInterface
    -   [MongoDBBSONDecimal128Interface](class.mongodb-bson-decimal128interface.html) - Інтерфейс MongoDBBSONDecimal128Interface
    -   [MongoDBBSONJavascriptInterface](class.mongodb-bson-javascriptinterface.html) - Інтерфейс MongoDBBSONJavascriptInterface
    -   [MongoDBBSONMaxKeyInterface](class.mongodb-bson-maxkeyinterface.html) - Інтерфейс MongoDBBSONMaxKeyInterface
    -   [MongoDBBSONMinKeyInterface](class.mongodb-bson-minkeyinterface.html) - Інтерфейс MongoDBBSONMinKeyInterface
    -   [MongoDBBSONObjectIdInterface](class.mongodb-bson-objectidinterface.html) - Інтерфейс MongoDBBSONObjectIdInterface
    -   [MongoDBBSONRegexInterface](class.mongodb-bson-regexinterface.html) - Інтерфейс MongoDBBSONRegexInterface
    -   [MongoDBBSONTimestampInterface](class.mongodb-bson-timestampinterface.html) - Інтерфейс MongoDBBSONTimestampInterface
    -   [MongoDBBSONUTCDateTimeInterface](class.mongodb-bson-utcdatetimeinterface.html) - Інтерфейс MongoDBBSONUTCDateTimeInterface
    -   [MongoDBBSONDBPointer](class.mongodb-bson-dbpointer.html) - Клас MongoDBBSONDBPointer (застарілий)
    -   [MongoDBBSONInt64](class.mongodb-bson-int64.html) - Клас MongoDBBSONInt64
    -   [MongoDBBSONSymbol](class.mongodb-bson-symbol.html) - Клас MongoDBBSONSymbol (застарілий)
    -   [MongoDBBSONUndefined](class.mongodb-bson-undefined.html) - Клас MongoDBBSONUndefined (застаріло)
-   [MongoDBDriverMonitoring](mongodb.monitoring.html) — Класи моніторингу та функції передплатника
    -   [Функції](ref.monitoring.functions.html)
    -   [MongoDBDriverMonitoringCommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html) - Клас MongoDBDriverMonitoringCommandFailedEvent
    -   [MongoDBDriverMonitoringCommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html) - Клас MongoDBDriverMonitoringCommandStartedEvent
    -   [MongoDBDriverMonitoringCommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html) - Клас MongoDBDriverMonitoringCommandSucceedEvent
    -   [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html) - Клас MongoDBDriverMonitoringServerChangedEvent
    -   [MongoDBDriverMonitoringServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html) - Клас MongoDBDriverMonitoringServerClosedEvent
    -   [MongoDBDriverMonitoringServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html) - Клас MongoDBDriverMonitoringServerOpeningEvent
    -   [MongoDBDriverMonitoringServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatFailedEvent
    -   [MongoDBDriverMonitoringServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent
    -   [MongoDBDriverMonitoringServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent
    -   [MongoDBDriverMonitoringTopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html) - Клас MongoDBDriverMonitoringTopologyChangedEvent
    -   [MongoDBDriverMonitoringTopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.html) - Клас MongoDBDriverMonitoringTopologyClosedEvent
    -   [MongoDBDriverMonitoringTopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html) - Клас MongoDBDriverMonitoringTopologyOpeningEvent
    -   [MongoDBDriverMonitoringCommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html) - Інтерфейс The MongoDBDriverMonitoringCommandSubscriber
    -   [MongoDBDriverMonitoringSDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html) - Інтерфейс MongoDBDriverMonitoringSDAMSubscriber
    -   [MongoDBDriverMonitoringSubscriber](class.mongodb-driver-monitoring-subscriber.html) - Інтерфейс MongoDBDriverMonitoringSubscriber
-   [MongoDBDriverException](mongodb.exceptions.html) - Класи винятків
    -   [MongoDBDriverExceptionAuthenticationException](class.mongodb-driver-exception-authenticationexception.html) - Клас MongoDBDriverExceptionAuthenticationException
    -   [MongoDBDriverExceptionBulkWriteException](class.mongodb-driver-exception-bulkwriteexception.html) - Клас MongoDBDriverExceptionBulkWriteException
    -   [MongoDBDriverExceptionCommandException](class.mongodb-driver-exception-commandexception.html) - Клас MongoDBDriverExceptionCommandException
    -   [MongoDBDriverExceptionConnectionException](class.mongodb-driver-exception-connectionexception.html) - Клас MongoDBDriverExceptionConnectionException
    -   [MongoDBDriverExceptionConnectionTimeoutException](class.mongodb-driver-exception-connectiontimeoutexception.html) - Клас MongoDBDriverExceptionConnectionTimeoutException
    -   [MongoDBDriverExceptionEncryptionException](class.mongodb-driver-exception-encryptionexception.html) - Клас MongoDBDriverExceptionEncryptionException
    -   [MongoDBDriverExceptionException](class.mongodb-driver-exception-exception.html) - Інтерфейс MongoDBDriverExceptionException
    -   [MongoDBDriverExceptionExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.html) - Клас MongoDBDriverExceptionExecutionTimeoutException
    -   [MongoDBDriverExceptionInvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) - Клас MongoDBDriverExceptionInvalidArgumentException
    -   [MongoDBDriverExceptionLogicException](class.mongodb-driver-exception-logicexception.html) - Клас MongoDBDriverExceptionLogicException
    -   [MongoDBDriverExceptionRuntimeException](class.mongodb-driver-exception-runtimeexception.html) - Клас MongoDBDriverExceptionRuntimeException
    -   [MongoDBDriverExceptionServerException](class.mongodb-driver-exception-serverexception.html) - Клас MongoDBDriverExceptionServerException
    -   [MongoDBDriverExceptionSSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.html) - Клас MongoDBDriverExceptionSSLConnectionException (застарілий)
    -   [MongoDBDriverExceptionUnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) - Клас MongoDBDriverExceptionUnexpectedValueException
    -   [MongoDBDriverExceptionWriteException](class.mongodb-driver-exception-writeexception.html) - Клас MongoDBDriverExceptionWriteException
    -   [Class Tree](mongodb.exceptions.tree.html) - MongoDB Exception Class Tree