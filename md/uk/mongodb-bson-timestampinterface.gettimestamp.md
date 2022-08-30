Повертає компонент позначки часу TimestampInterface

-   [« MongoDBBSONTimestampInterface::getIncrement](mongodb-bson-timestampinterface.getincrement.html)
    
-   [MongoDBBSONTimestampInterface::toString »](mongodb-bson-timestampinterface.tostring.html)
    
-   [PHP Manual](index.html)
    
-   [MongoDBBSONTimestampInterface](class.mongodb-bson-timestampinterface.html)
    
-   Повертає компонент позначки часу TimestampInterface
    

# MongoDBBSONTimestampInterface::getTimestamp

(mongodb >=1.3.0)

MongoDBBSONTimestampInterface::getTimestamp — Повертає компонент позначки часу TimestampInterface

### Опис

```methodsynopsis
abstract public MongoDB\BSON\TimestampInterface::getTimestamp(): int
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає компонент позначки часу TimestampInterface.

**Увага**

У 32-бітових системах цей метод може повертати негативне число. Хоча частини збільшення та позначки часу типу позначки часу BSON складаються з двох 32-розрядних значень без знака, PHP не може представляти їх на 32-розрядних платформах.

### Дивіться також

-   [MongoDBBSONTimestamp::getTimestamp()](mongodb-bson-timestamp.gettimestamp.html) - Повертає компонент позначки часу Timestamp