Повертає базу подій, пов'язану зі з'єднанням

-   [« EventHttpConnection::construct](eventhttpconnection.construct.html)
    
-   [EventHttpConnection::getPeer »](eventhttpconnection.getpeer.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttpConnection](class.eventhttpconnection.html)
    
-   Повертає базу подій, пов'язану зі з'єднанням
    

# EventHttpConnection::getBase

(PECL event >= 1.2.6-beta)

EventHttpConnection::getBase — Повертає базу подій, пов'язану зі з'єднанням

### Опис

```methodsynopsis
public
   EventHttpConnection::getBase(): EventBase
```

Повертає основу подій, пов'язану зі з'єднанням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт [EventBase](class.eventbase.html), пов'язаний із з'єднанням. В іншому випадку - **`false`**