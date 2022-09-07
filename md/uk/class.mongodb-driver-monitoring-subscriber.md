---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologyopening.md: '« MongoDBDriverMonitoringSDAMSubscriber::topologyOpening'
  - mongodb.exceptions.md: MongoDBDriverException »
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDBDriverMonitoring
title: Інтерфейс MongoDBDriverMonitoringSubscriber
---
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
