Повертає інкрементний компонент TimestampInterface

-   [« MongoDB\\BSON\\TimestampInterface](class.mongodb-bson-timestampinterface.html)
    
-   [MongoDB\\BSON\\TimestampInterface::getTimestamp »](mongodb-bson-timestampinterface.gettimestamp.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDB\\BSON\\TimestampInterface](class.mongodb-bson-timestampinterface.html)
    
-   Повертає інкрементний компонент TimestampInterface
    

# MongoDBBSONTimestampInterface::getIncrement

(mongodb >=1.3.0)

MongoDBBSONTimestampInterface::getIncrement — Повертає інкрементний компонент TimestampInterface

### Опис

```methodsynopsis
abstract public MongoDB\BSON\TimestampInterface::getIncrement(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає інкрементний компонент TimestampInterface.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представляти їх на 32-розрядних платформах.

### Дивіться також

-   [MongoDB\\BSON\\Timestamp::getIncrement()](mongodb-bson-timestamp.getincrement.html) - Повертає компонент збільшення Timestamp