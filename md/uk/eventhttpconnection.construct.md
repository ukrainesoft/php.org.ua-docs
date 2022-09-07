---
navigation:
  - class.eventhttpconnection.md: « EventHttpConnection
  - eventhttpconnection.getbase.md: 'EventHttpConnection::getBase »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::construct'
---
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

Об'єкт класу [EventSslContext](class.eventsslcontext.md). Включає OpenSSL.

> **Зауваження**
> 
> Цей параметр доступний, лише якщо `Event` скомпільований за допомогою OpenSSL і тільки з `Libevent 2.1.0-alpha` і вище.

### Значення, що повертаються

Повертає об'єкт [EventHttpConnection](class.eventhttpconnection.md)

### список змін

| Версия | Описание |
| --- | --- |
| PECL event 1.9.0 | Додана підтримка OpenSSL (`ctx` |
