Інтерфейс MongoDBDriverMonitoringSubscriber

-   [« MongoDBDriverMonitoringSDAMSubscriber::topologyOpening](mongodb-driver-monitoring-sdamsubscriber.topologyopening.html)
    
-   [MongoDBDriverException »](mongodb.exceptions.md)
    
-   [PHP Manual](index.md)
    
-   [MongoDBDriverMonitoring](mongodb.monitoring.md)
    
-   Інтерфейс MongoDBDriverMonitoringSubscriber
    

# Інтерфейс MongoDBDriverMonitoringSubscriber

(mongodb >=1.3.0)

## Вступ

Базовий інтерфейс для передплатників подій Використовується як тип параметра у функціях [MongoDBDriverMonitoringaddSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) і [MongoDBDriverMonitoringremoveSubscriber()](function.mongodb.driver.monitoring.removesubscriber.md), і має реалізовуватися напряму.

## Огляд інтерфейсів

```synopsis


    
    
     
      class MongoDB\Driver\Monitoring\Subscriber
     
     {
    

   }
```

Цей інтерфейс немає методів. Його єдина мета – бути базовим інтерфейсом для всіх передплатників подій.