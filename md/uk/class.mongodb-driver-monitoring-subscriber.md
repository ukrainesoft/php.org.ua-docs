---
navigation:
  - mongodb-driver-monitoring-sdamsubscriber.topologyopening.md: '« MongoDB\\Driver\\Monitoring\\SDAMSubscriber::topologyOpening'
  - mongodb.exceptions.md: MongoDB\\Driver\\Exception »
  - index.md: PHP Manual
  - mongodb.monitoring.md: MongoDB\\Driver\\Monitoring
title: Інтерфейс MongoDB\\Driver\\Monitoring\\Subscriber
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс MongoDB\\Driver\\Monitoring\\Subscriber

(mongodb >=1.3.0)

## Вступ

Базовий інтерфейс для передплатників подій Використовується як тип параметра у функціях [MongoDB\\Driver\\Monitoring\\addSubscriber()](function.mongodb.driver.monitoring.addsubscriber.md) і [MongoDB\\Driver\\Monitoring\\removeSubscriber()](function.mongodb.driver.monitoring.removesubscriber.md), і має реалізовуватися напряму.

## Огляд інтерфейсів

```classsynopsis


    
    
     
      class MongoDB\Driver\Monitoring\Subscriber
     
     {
    

   }
```

Цей інтерфейс немає методів. Його єдина мета – бути базовим інтерфейсом для всіх передплатників подій.
