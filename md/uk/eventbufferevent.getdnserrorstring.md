Повертає рядок, що описує останню невдалу спробу пошуку DNS

-   [« EventBufferEvent::free](eventbufferevent.free.html)
    
-   [EventBufferEvent::getEnabled »](eventbufferevent.getenabled.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Повертає рядок, що описує останню невдалу спробу пошуку DNS
    

# EventBufferEvent::getDnsErrorString

(PECL event >= 1.2.6-beta)

EventBufferEvent::getDnsErrorString — Повертає рядок, що описує останню невдалу спробу пошуку DNS

### Опис

```methodsynopsis
public
   EventBufferEvent::getDnsErrorString(): string
```

Повертає рядок, що описує останню невдалу спробу пошуку DNS, зроблену [EventBufferEvent::connectHost()](eventbufferevent.connecthost.html), або порожній рядок, якщо помилку DNS не виявлено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що описує помилку пошуку DNS або порожній рядок, якщо помилки не відбулося.

### Дивіться також

-   [EventBufferEvent::connectHost()](eventbufferevent.connecthost.html) - Підключається на ім'я хоста з можливістю асинхронного дозволу DNS