Конструктор контексту OpenSSL для використання у класах Event

-   [« EventSslContext](class.eventsslcontext.md)
    
-   [EventUtil »](class.eventutil.md)
    
-   [PHP Manual](index.md)
    
-   [EventSslContext](class.eventsslcontext.md)
    
-   Конструктор контексту OpenSSL для використання у класах Event
    

# EventSslContext::construct

(PECL event >= 1.2.6-beta)

EventSslContext::construct — Конструктор контексту OpenSSL для використання у класах Event

### Опис

```methodsynopsis
public
   EventSslContext::__construct(
    string
     $method
   , 
    string
     $options
   )
```

Створює контекст SSL, що містить покажчик на `SSL_CTX` (Дивіться системне керівництво).

### Список параметрів

`method`

Одна з констант [`EventSslContext::*_METHOD`](class.eventsslcontext.html#eventsslcontext.constants)

`options`

Асоціативний масив опцій контексту SSL. Константи [`EventSslContext::OPT_*`](class.eventsslcontext.html#eventsslcontext.constants)

### Значення, що повертаються

Повертає об'єкт [EventSslContext](class.eventsslcontext.md)

### Приклади

**Приклад #1 Приклад використання **EventSslContext::construct()****

```php
<?php
$ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, array(
     EventSslContext::OPT_LOCAL_CERT        => $local_cert,
     EventSslContext::OPT_LOCAL_PK          => $local_pk,
     EventSslContext::OPT_PASSPHRASE        => "echo server",
     EventSslContext::OPT_VERIFY_PEER       => true,
     EventSslContext::OPT_ALLOW_SELF_SIGNED => false,
));
?>
```