---
navigation:
  - class.eventhttpconnection.md: « EventHttpConnection
  - eventhttpconnection.getbase.md: 'EventHttpConnection::getBase »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpConnection::\_\_construct

(PECL event >= 1.2.6-beta)

EventHttpConnection::\_\_construct — Створює об'єкт EventHttpConnection

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

Створює об'єкт EventHttpConnection.

### Список параметрів

`base`

Пов'язана основа подій.

`dns_base`

Якщо параметр `dns_base`равен\*\*`null`\*\*, дозвіл імені хоста буде заблоковано.

`address`

Адреса для підключення.

`port`

Порт для підключення.

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.md)Включает OpenSSL.

> **Зауваження** :
> 
> Параметр доступний, лише якщо модуль `Event` скомпільований за допомогою бібліотеки OpenSSL і тільки з модулем `Libevent 2.1.0-alpha` і вище.

### список змін

| Версия | Опис |
| --- | --- |
| PECL event 1.9.0 | Додано підтримку бібліотеки OpenSSL (`ctx` |
