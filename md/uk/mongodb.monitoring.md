Класи моніторингу та функції передплатника

-   [« MongoDB\\BSON\\Undefined::unserialize](mongodb-bson-undefined.unserialize.html)
    
-   [Функции »](ref.monitoring.functions.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB](set.mongodb.html)
    
-   Класи моніторингу та функції передплатника
    

# Класи моніторингу та функції передплатника

-   [Функции](ref.monitoring.functions.html)
    -   [MongoDB\\Driver\\Monitoring\\addSubscriber](function.mongodb.driver.monitoring.addsubscriber.html) - Глобальна реєстрація передплатника на подію моніторингу
    -   [MongoDB\\Driver\\Monitoring\\removeSubscriber](function.mongodb.driver.monitoring.removesubscriber.html) — Скасує глобальну реєстрацію передплатника на подію моніторингу
-   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent](class.mongodb-driver-monitoring-commandfailedevent.html) - Клас MongoDBDriverMonitoringCommandFailedEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getCommandName](mongodb-driver-monitoring-commandfailedevent.getcommandname.html) - Повертає ім'я команди
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getDurationMicros](mongodb-driver-monitoring-commandfailedevent.getdurationmicros.html) — Повертає тривалість команди у мікросекундах
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getError](mongodb-driver-monitoring-commandfailedevent.geterror.html) — Повертає виняток, пов'язаний із невдалою командою
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getOperationId](mongodb-driver-monitoring-commandfailedevent.getoperationid.html) - Повертає ідентифікатор операції команди
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getReply](mongodb-driver-monitoring-commandfailedevent.getreply.html) - Повертає документ відповіді команди
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getRequestId](mongodb-driver-monitoring-commandfailedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServer](mongodb-driver-monitoring-commandfailedevent.getserver.html) — Повертає сервер, на якому було виконано команду
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServerConnectionId](mongodb-driver-monitoring-commandfailedevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
    -   [MongoDB\\Driver\\Monitoring\\CommandFailedEvent::getServiceId](mongodb-driver-monitoring-commandfailedevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди
-   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent](class.mongodb-driver-monitoring-commandstartedevent.html) - Клас MongoDBDriverMonitoringCommandStartedEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommand](mongodb-driver-monitoring-commandstartedevent.getcommand.html) - Повертає документ команди
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getCommandName](mongodb-driver-monitoring-commandstartedevent.getcommandname.html) - Повертає ім'я команди
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getDatabaseName](mongodb-driver-monitoring-commandstartedevent.getdatabasename.html) — Повертає базу даних, на якій виконувалась команда
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getOperationId](mongodb-driver-monitoring-commandstartedevent.getoperationid.html) - Повертає ідентифікатор операції команди
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getRequestId](mongodb-driver-monitoring-commandstartedevent.getrequestid.html) - Повертає ідентифікатор запиту команди
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServer](mongodb-driver-monitoring-commandstartedevent.getserver.html) — Повертає сервер, на якому було виконано команду
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServerConnectionId](mongodb-driver-monitoring-commandstartedevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
    -   [MongoDB\\Driver\\Monitoring\\CommandStartedEvent::getServiceId](mongodb-driver-monitoring-commandstartedevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди
-   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent](class.mongodb-driver-monitoring-commandsucceededevent.html) - Клас MongoDBDriverMonitoringCommandSucceedEvent
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getCommandName](mongodb-driver-monitoring-commandsucceededevent.getcommandname.html) - Повертає ім'я команди
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getDurationMicros](mongodb-driver-monitoring-commandsucceededevent.getdurationmicros.html) — Повертає тривалість команди у мікросекундах
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getOperationId](mongodb-driver-monitoring-commandsucceededevent.getoperationid.html) - Повертає ідентифікатор операції команди
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getReply](mongodb-driver-monitoring-commandsucceededevent.getreply.html) - Повертає документ відповіді команди
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getRequestId](mongodb-driver-monitoring-commandsucceededevent.getrequestid.html) - Повертає ідентифікатор запиту команди
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServer](mongodb-driver-monitoring-commandsucceededevent.getserver.html) — Повертає сервер, на якому було виконано команду
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServerConnectionId](mongodb-driver-monitoring-commandsucceededevent.getserverconnectionid.html) — Повертає ідентифікатор з'єднання із сервером для команди
    -   [MongoDB\\Driver\\Monitoring\\CommandSucceededEvent::getServiceId](mongodb-driver-monitoring-commandsucceededevent.getserviceid.html) — Повертає ідентифікатор служби балансувальника навантаження для команди
-   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html) - Клас MongoDBDriverMonitoringServerChangedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getHost](mongodb-driver-monitoring-serverchangedevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getNewDescription](mongodb-driver-monitoring-serverchangedevent.getnewdescription.html) — Повертає новий опис сервера
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPort](mongodb-driver-monitoring-serverchangedevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getPreviousDescription](mongodb-driver-monitoring-serverchangedevent.getpreviousdescription.html) — Повертає попередній опис сервера
    -   [MongoDB\\Driver\\Monitoring\\ServerChangedEvent::getTopologyId](mongodb-driver-monitoring-serverchangedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером
-   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent](class.mongodb-driver-monitoring-serverclosedevent.html) - Клас MongoDBDriverMonitoringServerClosedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getHost](mongodb-driver-monitoring-serverclosedevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getPort](mongodb-driver-monitoring-serverclosedevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerClosedEvent::getTopologyId](mongodb-driver-monitoring-serverclosedevent.gettopologyid.html) — Повертає ідентифікатор топології, пов'язаний із цим сервером
-   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent](class.mongodb-driver-monitoring-serveropeningevent.html) - Клас MongoDBDriverMonitoringServerOpeningEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getHost](mongodb-driver-monitoring-serveropeningevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getPort](mongodb-driver-monitoring-serveropeningevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerOpeningEvent::getTopologyId](mongodb-driver-monitoring-serveropeningevent.gettopologyid.html) — Returns the topology ID associated with this server
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent](class.mongodb-driver-monitoring-serverheartbeatfailedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatFailedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatfailedevent.getdurationmicros.html) — Повертає тривалість heartbeat у мікросекундах
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getError](mongodb-driver-monitoring-serverheartbeatfailedevent.geterror.html) — Повертає виняток, пов'язаний із невдалим виконанням heartbeat
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getHost](mongodb-driver-monitoring-serverheartbeatfailedevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::getPort](mongodb-driver-monitoring-serverheartbeatfailedevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatFailedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatfailedevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent](class.mongodb-driver-monitoring-serverheartbeatstartedevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatStartedEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getHost](mongodb-driver-monitoring-serverheartbeatstartedevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::getPort](mongodb-driver-monitoring-serverheartbeatstartedevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatStartedEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatstartedevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол
-   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent](class.mongodb-driver-monitoring-serverheartbeatsucceededevent.html) - Клас MongoDBDriverMonitoringServerHeartbeatSucceededEvent
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getDurationMicros](mongodb-driver-monitoring-serverheartbeatsucceededevent.getdurationmicros.html) — Повертає тривалість heartbeat у мікросекундах
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getHost](mongodb-driver-monitoring-serverheartbeatsucceededevent.gethost.html) — Повертає ім'я сервера.
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getPort](mongodb-driver-monitoring-serverheartbeatsucceededevent.getport.html) — Повертає порт, на якому прослуховується сервер
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::getReply](mongodb-driver-monitoring-serverheartbeatsucceededevent.getreply.html) - Повертає документ відповіді heartbeat
    -   [MongoDB\\Driver\\Monitoring\\ServerHeartbeatSucceededEvent::isAwaited](mongodb-driver-monitoring-serverheartbeatsucceededevent.isawaited.html) — Повертає, чи використовувався в heartbeat потоковий протокол
-   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent](class.mongodb-driver-monitoring-topologychangedevent.html) - Клас MongoDBDriverMonitoringTopologyChangedEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getNewDescription](mongodb-driver-monitoring-topologychangedevent.getnewdescription.html) — Повертає новий опис топології
    -   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getPreviousDescription](mongodb-driver-monitoring-topologychangedevent.getpreviousdescription.html) — Повертає попередній опис топології
    -   [MongoDB\\Driver\\Monitoring\\TopologyChangedEvent::getTopologyId](mongodb-driver-monitoring-topologychangedevent.gettopologyid.html) - Повертає ідентифікатор топології
-   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent](class.mongodb-driver-monitoring-topologyclosedevent.html) - Клас MongoDBDriverMonitoringTopologyClosedEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyClosedEvent::getTopologyId](mongodb-driver-monitoring-topologyclosedevent.gettopologyid.html) - Повертає ідентифікатор топології
-   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent](class.mongodb-driver-monitoring-topologyopeningevent.html) - Клас MongoDBDriverMonitoringTopologyOpeningEvent
    -   [MongoDB\\Driver\\Monitoring\\TopologyOpeningEvent::getTopologyId](mongodb-driver-monitoring-topologyopeningevent.gettopologyid.html) - Повертає ідентифікатор топології
-   [MongoDB\\Driver\\Monitoring\\CommandSubscriber](class.mongodb-driver-monitoring-commandsubscriber.html) - Інтерфейс The MongoDBDriverMonitoringCommandSubscriber
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandFailed](mongodb-driver-monitoring-commandsubscriber.commandfailed.html) — Метод повідомлення про невдалу команду
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandStarted](mongodb-driver-monitoring-commandsubscriber.commandstarted.html) — Метод повідомлення про запущену команду
    -   [MongoDB\\Driver\\Monitoring\\CommandSubscriber::commandSucceeded](mongodb-driver-monitoring-commandsubscriber.commandsucceeded.html) — Метод сповіщення про успішну команду
-   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber](class.mongodb-driver-monitoring-sdamsubscriber.html) - Інтерфейс MongoDBDriverMonitoringSDAMSubscriber
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverChanged](mongodb-driver-monitoring-sdamsubscriber.serverchanged.html) — Метод сповіщення про зміну опису сервера
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverClosed](mongodb-driver-monitoring-sdamsubscriber.serverclosed.html) — Метод сповіщення про закриття сервера
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatFailed](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatfailed.html) — Метод повідомлення про невдалий heartbeat сервер
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatStarted](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatstarted.html) — Метод повідомлення про запущений heartbeat сервер
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverHeartbeatSucceeded](mongodb-driver-monitoring-sdamsubscriber.serverheartbeatsucceeded.html) — Метод повідомлення про успішний heartbeat сервер
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::serverOpening](mongodb-driver-monitoring-sdamsubscriber.serveropening.html) — Метод сповіщення про відкриття сервера
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyChanged](mongodb-driver-monitoring-sdamsubscriber.topologychanged.html) — Метод сповіщення про зміну опису топології
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyClosed](mongodb-driver-monitoring-sdamsubscriber.topologyclosed.html) — Метод сповіщення про закриття топології
    -   [MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html) — Метод сповіщення про відкриття топології
-   [MongoDB\\Driver\\Monitoring\\Subscriber](class.mongodb-driver-monitoring-subscriber.html) - Інтерфейс MongoDBDriverMonitoringSubscriber