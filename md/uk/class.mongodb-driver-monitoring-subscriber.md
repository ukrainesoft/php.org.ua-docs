Інтерфейс MongoDBDriverMonitoringSubscriber

-   [« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html)
    
-   [MongoDB\\Driver\\Exception »](mongodb.exceptions.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\Driver\\Monitoring](mongodb.monitoring.html)
    
-   Інтерфейс MongoDBDriverMonitoringSubscriber
    

# Інтерфейс MongoDBDriverMonitoringSubscriber

(mongodb >=1.3.0)

## Вступ

Базовий інтерфейс для передплатників подій Використовується як тип параметра у функціях [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) і [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html), і має реалізовуватися напряму.

## Огляд інтерфейсів

```synopsis


    
    
     
      class MongoDB\Driver\Monitoring\Subscriber
     
     {
    

   }
```

Цей інтерфейс немає методів. Його єдина мета – бути базовим інтерфейсом для всіх передплатників подій.