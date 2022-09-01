---
navigation:
  - mongodb-driver-server.issecondary.html: '« MongoDBDriverServer::isSecondary'
  - mongodb-driver-serverdescription.gethelloresponse.html: 'MongoDBDriverServerDescription::getHelloResponse »'
  - index.md: PHP Manual
  - book.mongodb.md: MongoDBDriver
title: Клас MongoDBDriverServerDescription
---
# Клас MongoDBDriverServerDescription

(mongodb >=1.13.0)

## Вступ

Клас **MongoDBDriverServerDescription** є об'єктом значення, що представляє сервер, до якого підключений драйвер. Примірники класу повертаються методами [MongoDBDriverServer::getServerDescription()](mongodb-driver-server.getserverdescription.html) і [MongoDBDriverMonitoringServerChangedEvent](class.mongodb-driver-monitoring-serverchangedevent.html)

## Огляд класів

```classsynopsis


    
    
     final
     
      class MongoDB\Driver\ServerDescription
     
     {
    
    /* Константы */
    
     const
     string
      TYPE_UNKNOWN = "Unknown";

    const
     string
      TYPE_STANDALONE = "Standalone";

    const
     string
      TYPE_MONGOS = "Mongos";

    const
     string
      TYPE_POSSIBLE_PRIMARY = "PossiblePrimary";

    const
     string
      TYPE_RS_PRIMARY = "RSPrimary";

    const
     string
      TYPE_RS_SECONDARY = "RSSecondary";

    const
     string
      TYPE_RS_ARBITER = "RSArbiter";

    const
     string
      TYPE_RS_OTHER = "RSOther";

    const
     string
      TYPE_RS_GHOST = "RSGhost";

    const
     string
      TYPE_LOAD_BALANCER = "LoadBalancer";


    /* Методы */
    
   final public getHelloResponse(): array
final public getHost(): string
final public getLastUpdateTime(): int
final public getPort(): int
final public getRoundTripTime(): ?int
final public getType(): string

   }
```

## Обумовлені константи

**`MongoDB\Driver\ServerDescription::TYPE_UNKNOWN`**

Невідомий тип сервера, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_STANDALONE`**

Тип автономного сервера, який повертається методом[MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_MONGOS`**

Тип сервера Mongos, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_POSSIBLE_PRIMARY`**

Набір реплік можливого типу первинного сервера, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

Сервер може бути визначений як можливий первинний, якщо він ще не був перевірений, але інша пам'ять реплік набору вважає його первинним.

**`MongoDB\Driver\ServerDescription::TYPE_RS_PRIMARY`**

Тип первинного сервера набору реплік, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_RS_SECONDARY`**

Тип вторинного сервера набору реплік, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_RS_ARBITER`**

Тип сервера арбітражу набору реплік, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

**`MongoDB\Driver\ServerDescription::TYPE_RS_OTHER`**

Набір реплік іншого типу сервера, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

Такі сервери можуть бути приховані, запускатися чи відновлюватися. Їх не можна запитати, але їх списки хостів корисні для виявлення поточної конфігурації набору реплік.

**`MongoDB\Driver\ServerDescription::TYPE_RS_GHOST`**

Тип сервера-примари набору реплік, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

Сервери можуть бути визначені принаймні в трьох ситуаціях: короткочасно під час запуску сервера; у неініціалізованому наборі реплік; або коли сервер уникає (тобто видаляється з конфігурації набору реплік). Вони можуть бути запитані, і їх список хостів може бути використаний виявлення поточної конфігурації набору реплік; Однак клієнт може стежити за цим сервером, сподіваючись, що він перейде в більш корисний стан.

**`MongoDB\Driver\ServerDescription::TYPE_LOAD_BALANCER`**

Тип сервера балансувальника навантаження, який повертається методом [MongoDBDriverServerDescription::getType()](mongodb-driver-serverdescription.gettype.html)

## Зміст

-   [MongoDBDriverServerDescription::getHelloResponse](mongodb-driver-serverdescription.gethelloresponse.html) - Повертає останню відповідь сервера "hello"
-   [MongoDBDriverServerDescription::getHost](mongodb-driver-serverdescription.gethost.html) — Повертає ім'я сервера.
-   [MongoDBDriverServerDescription::getLastUpdateTime](mongodb-driver-serverdescription.getlastupdatetime.html) — Повертає час останнього оновлення сервера у мікросекундах
-   [MongoDBDriverServerDescription::getPort](mongodb-driver-serverdescription.getport.html) — Повертає порт, на якому прослуховується цей сервер
-   [MongoDBDriverServerDescription::getRoundTripTime](mongodb-driver-serverdescription.getroundtriptime.html) — Повертає час обходу сервера у мілісекундах
-   [MongoDBDriverServerDescription::getType](mongodb-driver-serverdescription.gettype.html) — Повертає рядок, який позначає тип сервера
