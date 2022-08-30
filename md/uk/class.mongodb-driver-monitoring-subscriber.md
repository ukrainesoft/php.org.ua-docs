Інтерфейс MongoDBDriverMonitoringSubscriber

-   [« MongoDBDriverMonitoringSDAMSubscriber::topologyOpening](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html)
    
-   [MongoDBDriverException »](mongodb.exceptions.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.html)
    
-   Інтерфейс MongoDBDriverMonitoringSubscriber
    

# Інтерфейс MongoDBDriverMonitoringSubscriber

(mongodb >=1.3.0)

## Вступ

Базовий інтерфейс для передплатників подій Використовується як тип параметра у функціях [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.html) і [MongoDBDriverMonitoringremoveSubscriber()](function.mongodb.driver.monitoring.removesubscriber.html), і має реалізовуватися напряму.

## Огляд інтерфейсів

```synopsis


    
    
     
      class MongoDB\Driver\Monitoring\Subscriber
     
     {
    

   }
```

Цей інтерфейс немає методів. Його єдина мета – бути базовим інтерфейсом для всіх передплатників подій.