Повертає об'єкт EventHttpConnection

-   [« EventHttpRequest::getCommand](eventhttprequest.getcommand.html)
    
-   [EventHttpRequest::getHost »](eventhttprequest.gethost.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttpRequest](class.eventhttprequest.html)
    
-   Повертає об'єкт EventHttpConnection
    

# EventHttpRequest::getConnection

(PECL event >= 1.8.0)

EventHttpRequest::getConnection — Повертає об'єкт EventHttpConnection

### Опис

```methodsynopsis
public
   EventHttpRequest::closeConnection(): EventHttpConnection
```

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.html), що представляє з'єднання HTTP, пов'язане з запитом.

**Увага**

Libevent API дозволяє об'єктам HTTP-запиту не прив'язуватися до жодного HTTP-з'єднання. Тому ми не можемо однозначно пов'язати [EventHttpRequest](class.eventhttprequest.html) з [EventHttpConnection](class.eventhttpconnection.html). Таким чином, ми створюємо об'єкт [EventHttpConnection](class.eventhttpconnection.html) на льоту. Не маючи інформації про базу подій, базу DNS та callback-функції при закритті з'єднання, ми просто залишаємо ці поля незаповненими.

Метод **EventHttpRequest::getConnection()** зазвичай корисний, коли нам потрібно реалізувати callback-функцію при закритті з'єднання. Дивіться [EventHttpConnection::setCloseCallback()](eventhttpconnection.setclosecallback.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.html)

### Дивіться також

-   [EventHttpConnection::setCloseCallback()](eventhttpconnection.setclosecallback.html) - Встановлює callback-функцію при закритті з'єднання
-   [EventHttpRequest::getBufferEvent()](eventhttprequest.getbufferevent.html) - Повертає об'єкт EventBufferEvent