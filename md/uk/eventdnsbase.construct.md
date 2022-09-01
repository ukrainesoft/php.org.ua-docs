---
navigation:
  - eventdnsbase.clearsearch.html: '« EventDnsBase::clearSearch'
  - eventdnsbase.countnameservers.html: 'EventDnsBase::countNameservers »'
  - index.html: PHP Manual
  - class.eventdnsbase.html: EventDnsBase
title: 'EventDnsBase::construct'
---
# EventDnsBase::construct

(PECL event >= 1.2.6-beta)

EventDnsBase::construct — Конструктор об'єкта EventDnsBase

### Опис

```methodsynopsis
public
   EventDnsBase::__construct(
    EventBase
     $base
   , 
    bool
     $initialize
   )
```

Конструктор об'єкта EventDnsBase.

### Список параметрів

`base`

Основа подій.

`initialize`

Якщо аргумент `initialize` має значення **`true`**, він намагається розумно налаштувати базу DNS з урахуванням параметрів операційної системи за промовчанням. В іншому випадку база подій DNS залишається порожньою, без налаштованих серверів імен або параметрів. В останньому випадку база DNS має бути налаштована вручну, наприклад, за допомогою [EventDnsBase::parseResolvConf()](eventdnsbase.parseresolvconf.html)

### Значення, що повертаються

Повертає об'єкт EventDnsBase.
