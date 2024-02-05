---
navigation:
  - class.eventsslcontext.md: « EventSslContext
  - class.eventutil.md: EventUtil »
  - index.md: PHP Manual
  - class.eventsslcontext.md: EventSslContext
title: 'EventSslContext::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventSslContext::\_\_construct

(PECL event >= 1.2.6-beta)

EventSslContext::\_\_construct — Створює контекст OpenSSL для класів модуля Event

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

Створює контекст SSL, що містить покажчик на об'єкт контексту `SSL_CTX`(смотрите системное руководство).

### Список параметрів

`method`

Константа семейства[`EventSslContext::*_METHOD`](class.eventsslcontext.md#eventsslcontext.constants)

`options`

Асоціативний масив опцій контексту SSL. Константи [`EventSslContext::OPT_*`](class.eventsslcontext.md#eventsslcontext.constants)

### Приклади

**Пример #1 Пример использования метода**EventSslContext::\_\_construct()\*\*\*\*

```php
<?php

$ctx = new EventSslContext(EventSslContext::SSLv3_SERVER_METHOD, array(
     EventSslContext::OPT_LOCAL_CERT        => $local_cert,
     EventSslContext::OPT_LOCAL_PK          => $local_pk,
     EventSslContext::OPT_PASSPHRASE        => "echo server",
     EventSslContext::OPT_VERIFY_PEER       => true,
     EventSslContext::OPT_ALLOW_SELF_SIGNED => false,
));

?>
```
