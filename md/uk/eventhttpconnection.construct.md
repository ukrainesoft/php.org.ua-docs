Конструктор об'єкта EventHttpConnection

-   [« EventHttpConnection](class.eventhttpconnection.html)
    
-   [EventHttpConnection::getBase »](eventhttpconnection.getbase.html)
    
-   [PHP Manual](index.html)
    
-   [EventHttpConnection](class.eventhttpconnection.html)
    
-   Конструктор об'єкта EventHttpConnection
    

# EventHttpConnection::construct

(PECL event >= 1.2.6-beta)

EventHttpConnection::construct — Конструктор об'єкта EventHttpConnection

### Опис

```methodsynopsis
public
   EventHttpConnection::__construct(    
    EventBase
     $base
   ,    
    EventDnsBase
     $dns_base
   ,    
    string
     $address
   ,    
    int
     $port
   ,    
    EventSslContext
     $ctx
     = null
   )
```

Конструктор об'єкта EventHttpConnection.

### Список параметрів

`base`

Пов'язана основа подій.

`dns_base`

Якщо параметр `dns_base` дорівнює **`null`**, дозвіл імені хоста буде заблоковано.

`address`

Адреса для підключення.

`port`

Порт для підключення.

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.html). Включає OpenSSL.

> **Зауваження**
> 
> Цей параметр доступний, лише якщо `Event` скомпільований за допомогою OpenSSL і тільки з `Libevent 2.1.0-alpha` і вище.

### Значення, що повертаються

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.html)

### список змін

| Версия           | Описание                        |
|------------------|---------------------------------|
| PECL event 1.9.0 | Додана підтримка OpenSSL (`ctx` |