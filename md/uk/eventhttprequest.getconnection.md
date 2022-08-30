Повертає об'єкт EventHttpConnection

-   [« EventHttpRequest::getCommand](eventhttprequest.getcommand.md)
    
-   [EventHttpRequest::getHost »](eventhttprequest.gethost.md)
    
-   [PHP Manual](index.md)
    
-   [EventHttpRequest](class.eventhttprequest.md)
    
-   Повертає об'єкт EventHttpConnection
    

# EventHttpRequest::getConnection

(PECL event >= 1.8.0)

EventHttpRequest::getConnection — Повертає об'єкт EventHttpConnection

### Опис

```methodsynopsis
public
   EventHttpRequest::closeConnection(): EventHttpConnection
```

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.md), що представляє з'єднання HTTP, пов'язане з запитом.

**Увага**

Libevent API дозволяє об'єктам HTTP-запиту не прив'язуватися до жодного HTTP-з'єднання. Тому ми не можемо однозначно пов'язати [EventHttpRequest](class.eventhttprequest.md) з [EventHttpConnection](class.eventhttpconnection.md). Таким чином, ми створюємо об'єкт [EventHttpConnection](class.eventhttpconnection.md) на льоту. Не маючи інформації про базу подій, базу DNS та callback-функції при закритті з'єднання, ми просто залишаємо ці поля незаповненими.

Метод **EventHttpRequest::getConnection()** зазвичай корисний, коли нам потрібно реалізувати callback-функцію при закритті з'єднання. Дивіться [EventHttpConnection::setCloseCallback()](eventhttpconnection.setclosecallback.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.md)

### Дивіться також

-   [EventHttpConnection::setCloseCallback()](eventhttpconnection.setclosecallback.md) - Встановлює callback-функцію при закритті з'єднання
-   [EventHttpRequest::getBufferEvent()](eventhttprequest.getbufferevent.md) - Повертає об'єкт EventBufferEvent