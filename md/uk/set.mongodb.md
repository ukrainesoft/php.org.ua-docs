Драйвер MongoDB

-   [« db2\_tables](function.db2-tables.html)
    
-   [Установка и настройка »](mongodb.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для работы с базами данных отдельных производителей](refs.database.vendors.html)
    
-   Драйвер MongoDB
    

# Драйвер MongoDB

Цей модуль розроблено на основі бібліотек [» libmongoc](https://github.com/mongodb/mongo-c-driver) і [» libbson](https://github.com/mongodb/mongo-c-driver/tree/master/src/libbson). Він надає мінімальне API для ключового функціоналу драйвера: [команды](class.mongodb-driver-command.html) [запросы](class.mongodb-driver-query.html) [записи](class.mongodb-driver-bulkwrite.html) [управление соединением](class.mongodb-driver-manager.html) і [сериализация BSON](book.bson.html)

Саморобні бібліотеки PHP, що вимагають цей модуль, можуть надавати високорівневі API, такі як: збирачі запитів, методи-помічники для індивідуальних команд та GridFS. Розробники додатків повинні розглянути питання щодо використання цього модуля спільно з [» библиотекой MongoDB PHP](https://github.com/mongodb/mongo-php-library), яка реалізує такі ж високорівневі драйвери API MongoDB, як і для інших мов. Подібний поділ завдань дозволяє цьому драйверу сконцентруватися на головних завданнях, що стоять перед ним – підвищення продуктивності.

-   [Установка и настройка](mongodb.setup.html)
    -   [Требования](mongodb.requirements.html)
    -   [Установка](mongodb.installation.html)
    -   [Настройка во время выполнения](mongodb.configuration.html)
    -   [Предопределённые константы](mongodb.constants.html)
-   [Обучающие материалы](mongodb.tutorial.html)
    -   [Использование библиотеки PHP для MongoDB (PHPLIB)](mongodb.tutorial.library.html)
    -   [Мониторинг производительности приложения (Application Performance Monitoring или APM)](mongodb.tutorial.apm.html)
-   [Архитектура и внутреннее устройство драйвера](mongodb.architecture.html) — Огляд архітектури драйвера та її особливостей
    -   [Архитектура](mongodb.overview.html) - Огляд архітектури
    -   [Соединения](mongodb.connection-handling.html) — Обробка з'єднання та сталість
    -   [Постоянные данные](mongodb.persistence.html) — Серіалізація та десеріалізація змінних PHP у MongoDB
-   [Безопасность](mongodb.security.html)
    -   [Атака с помощью инъекций в запросе](mongodb.security.request_injection.html)
    -   [Атака с помощью инъекций в скриптах](mongodb.security.script_injection.html)
-   [MongoDB\\Driver](book.mongodb.html) - Класи драйвера MongoDB
    -   [MongoDB\\Driver\\Manager](class.mongodb-driver-manager.html) - Клас MongoDBDriverManager
    -   [MongoDB\\Driver\\Command](class.mongodb-driver-command.html) - Клас The MongoDBDriverCommand
    -   [MongoDB\\Driver\\Query](class.mongodb-driver-query.html) - Клас MongoDBDriverQuery
    -   [MongoDB\\Driver\\BulkWrite](class.mongodb-driver-bulkwrite.html) - Клас MongoDBDriverBulkWrite
    -   [MongoDB\\Driver\\Session](class.mongodb-driver-session.html) - Клас MongoDBDriverSession
    -   [MongoDB\\Driver\\ClientEncryption](class.mongodb-driver-clientencryption.html) - Клас MongoDBDriverClientEncryption
    -   [MongoDB\\Driver\\ServerApi](class.mongodb-driver-serverapi.html) - Клас MongoDBDriverServerApi
    -   [MongoDB\\Driver\\WriteConcern](class.mongodb-driver-writeconcern.html) - Клас MongoDBDriverWriteConcern
    -   [MongoDB\\Driver\\ReadPreference](class.mongodb-driver-readpreference.html) - Клас MongoDBDriverReadPreference
    -   [MongoDB\\Driver\\ReadConcern](class.mongodb-driver-readconcern.html) - Клас MongoDBDriverReadConcern
    -   [MongoDB\\Driver\\Cursor](class.mongodb-driver-cursor.html) - Клас MongoDBDriverCursor
    -   [MongoDB\\Driver\\CursorId](class.mongodb-driver-cursorid.html) - Клас MongoDBDriverCursorId
    -   [MongoDB\\Driver\\CursorInterface](class.mongodb-driver-cursorinterface.html) - Інтерфейс MongoDBDriverCursorInterface
    -   [MongoDB\\Driver\\Server](class.mongodb-driver-server.html) - Клас MongoDBDriverServer
    -   [MongoDB\\Driver\\ServerDescription](class.mongodb-driver-serverdescription.html) - Клас MongoDBDriverServerDescription
    -   [MongoDB\\Driver\\TopologyDescription](class.mongodb-driver-topologydescription.html) - Клас MongoDBDriverTopologyDescription
    -   [MongoDB\\Driver\\WriteConcernError](class.mongodb-driver-writeconcernerror.html) - Клас The MongoDBDriverWriteConcernError
    -   [MongoDB\\Driver\\WriteError](class.mongodb-driver-writeerror.html) - Клас MongoDBDriverWriteError
    -   [MongoDB\\Driver\\WriteResult](class.mongodb-driver-writeresult.html) - Клас MongoDBDriverWriteResult
-   [MongoDB\\BSON](book.bson.html) — Класи типів BSON та функції серіалізації
    -   [Функции](ref.bson.functions.html)
    -   [MongoDB\\BSON\\Binary](class.mongodb-bson-binary.html) - Клас MongoDBBSONBinary
    -   [MongoDB\\BSON\\Decimal128](class.mongodb-bson-decimal128.html) - Клас MongoDBBSONDecimal128
    -   [MongoDB\\BSON\\Javascript](class.mongodb-bson-javascript.html) - Клас MongoDBBSONJavascript
    -   [MongoDB\\BSON\\MaxKey](class.mongodb-bson-maxkey.html) - Клас MongoDBBSONMaxKey
    -   [MongoDB\\BSON\\MinKey](class.mongodb-bson-minkey.html) - Клас MongoDBBSONMinKey
    -   [MongoDB\\BSON\\ObjectId](class.mongodb-bson-objectid.html) - Клас MongoDBBSONObjectId
    -   [MongoDB\\BSON\\Regex](class.mongodb-bson-regex.html) - Клас MongoDBBSONRegex
    -   [MongoDB\\BSON\\Timestamp](class.mongodb-bson-timestamp.html) - Клас MongoDBBSONTimestamp
    -   [MongoDB\\BSON\\UTCDateTime](class.mongodb-bson-utcdatetime.html) - Клас MongoDBBSONUTCDateTime
    -   [MongoDB\\BSON\\Type](class.mongodb-bson-type.html) - Інтерфейс MongoDBBSONType
    -   [MongoDB\\BSON\\Persistable](class.mongodb-bson-persistable.html) - Інтерфейс MongoDBBSONPersistable
    -   [MongoDB\\BSON\\Serializable](class.mongodb-bson-serializable.html) - Інтерфейс MongoDBBSONSerializable
    -   [MongoDB\\BSON\\Unserializable](class.mongodb-bson-unserializable.html) - Інтерфейс MongoDBBSONUnserializable
    -   [MongoDB\\BSON\\BinaryInterface](class.mongodb-bson-binaryinterface.html) - Інтерфейс MongoDBBSONBinaryInterface
    -   [MongoDB\\BSON\\Decimal128Interface](class.mongodb-bson-decimal128interface.html) - Інтерфейс MongoDBBSONDecimal128Interface
    -   [MongoDB\\BSON\\JavascriptInterface](class.mongodb-bson-javascriptinterface.html) - Інтерфейс MongoDBBSONJavascriptInterface
    -   [MongoDB\\BSON\\MaxKeyInterface](class.mongodb-bson-maxkeyinterface.html) - Інтерфейс MongoDBBSONMaxKeyInterface
    -   [MongoDB\\BSON\\MinKeyInterface](class.mongodb-bson-minkeyinterface.html) - Інтерфейс MongoDBBSONMinKeyInterface
    -   [MongoDB\\BSON\\ObjectIdInterface](class.mongodb-bson-objectidinterface.html) - Інтерфейс MongoDBBSONObjectIdInterface
    -   [MongoDB\\BSON\\RegexInterface](class.mongodb-bson-regexinterface.html) - Інтерфейс MongoDBBSONRegexInterface
    -   [MongoDB\\BSON\\TimestampInterface](class.mongodb-bson-timestampinterface.html) - Інтерфейс MongoDBBSONTimestampInterface
    -   [MongoDB\\BSON\\UTCDateTimeInterface](class.mongodb-bson-utcdatetimeinterface.html) - Інтерфейс MongoDBBSONUTCDateTimeInterface
    -   [MongoDB\\BSON\\DBPointer](class.mongodb-bson-dbpointer.html) - Клас MongoDBBSONDBPointer (застарілий)
    -   [MongoDB\\BSON\\Int64](class.mongodb-bson-int64.html) - Клас MongoDBBSONInt64
    -   [MongoDB\\BSON\\Symbol](class.mongodb-bson-symbol.html) - Клас MongoDBBSONSymbol (застарілий)
    -   [MongoDB\\BSON\\Undefined](class.mongodb-bson-undefined.html) - Клас MongoDBBSONUndefined (застаріло)
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html) — Класи моніторингу та функції передплатника
    -   [Функции](ref.monitoring.functions.html)
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html) - Клас MongoDBDriverMonitoringCommandFailedEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html) - Клас MongoDBDriverMonitoringCommandStartedEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html) - Клас MongoDBDriverMonitoringCommandSucceedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html) - Клас MongoDBDriverMonitoringServerChangedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html) - Клас MongoDBDriverMonitoringServerClosedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html) - Клас MongoDBDriverMonitoringServerOpeningEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatFailedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html) - Клас MongoDBDriverMonitoringTopologyChangedEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.html) - Клас MongoDBDriverMonitoringTopologyClosedEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html) - Клас MongoDBDriverMonitoringTopologyOpeningEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html) - Інтерфейс The MongoDBDriverMonitoringCommandSubscriber
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html) - Інтерфейс MongoDBDriverMonitoringSDAMSubscriber
    -   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html) - Інтерфейс MongoDBDriverMonitoringSubscriber
-   [MongoDB\\Driver\\Exception](mongodb.exceptions.html) - Класи винятків
    -   [MongoDB\\Driver\\Exception\\AuthenticationException](class.mongodb-driver-exception-authenticationexception.html) - Клас MongoDBDriverExceptionAuthenticationException
    -   [MongoDB\\Driver\\Exception\\BulkWriteException](class.mongodb-driver-exception-bulkwriteexception.html) - Клас MongoDBDriverExceptionBulkWriteException
    -   [MongoDB\\Driver\\Exception\\CommandException](class.mongodb-driver-exception-commandexception.html) - Клас MongoDBDriverExceptionCommandException
    -   [MongoDB\\Driver\\Exception\\ConnectionException](class.mongodb-driver-exception-connectionexception.html) - Клас MongoDBDriverExceptionConnectionException
    -   [MongoDB\\Driver\\Exception\\ConnectionTimeoutException](class.mongodb-driver-exception-connectiontimeoutexception.html) - Клас MongoDBDriverExceptionConnectionTimeoutException
    -   [MongoDB\\Driver\\Exception\\EncryptionException](class.mongodb-driver-exception-encryptionexception.html) - Клас MongoDBDriverExceptionEncryptionException
    -   [MongoDB\\Driver\\Exception\\Exception](class.mongodb-driver-exception-exception.html) - Інтерфейс MongoDBDriverExceptionException
    -   [MongoDB\\Driver\\Exception\\ExecutionTimeoutException](class.mongodb-driver-exception-executiontimeoutexception.html) - Клас MongoDBDriverExceptionExecutionTimeoutException
    -   [MongoDB\\Driver\\Exception\\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.html) - Клас MongoDBDriverExceptionInvalidArgumentException
    -   [MongoDB\\Driver\\Exception\\LogicException](class.mongodb-driver-exception-logicexception.html) - Клас MongoDBDriverExceptionLogicException
    -   [MongoDB\\Driver\\Exception\\RuntimeException](class.mongodb-driver-exception-runtimeexception.html) - Клас MongoDBDriverExceptionRuntimeException
    -   [MongoDB\\Driver\\Exception\\ServerException](class.mongodb-driver-exception-serverexception.html) - Клас MongoDBDriverExceptionServerException
    -   [MongoDB\\Driver\\Exception\\SSLConnectionException](class.mongodb-driver-exception-sslconnectionexception.html) - Клас MongoDBDriverExceptionSSLConnectionException (застарілий)
    -   [MongoDB\\Driver\\Exception\\UnexpectedValueException](class.mongodb-driver-exception-unexpectedvalueexception.html) - Клас MongoDBDriverExceptionUnexpectedValueException
    -   [MongoDB\\Driver\\Exception\\WriteException](class.mongodb-driver-exception-writeexception.html) - Клас MongoDBDriverExceptionWriteException
    -   [Class Tree](mongodb.exceptions.tree.html) - MongoDB Exception Class Tree