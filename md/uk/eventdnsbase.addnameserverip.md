---
navigation:
  - class.eventdnsbase.html: « EventDnsBase
  - eventdnsbase.addsearch.html: 'EventDnsBase::addSearch »'
  - index.html: PHP Manual
  - class.eventdnsbase.html: EventDnsBase
title: 'EventDnsBase::addNameserverIp'
---
# EventDnsBase::addNameserverIp

(PECL event >= 1.2.6-beta)

EventDnsBase::addNameserverIp — Додає сервер імен до бази DNS

### Опис

```methodsynopsis
public
   EventDnsBase::addNameserverIp(
    string
     $ip
   ): bool
```

Додає сервер імен до бази evdnsbase.

### Список параметрів

`ip`

Рядок сервера імен у вигляді адреси IPv4, IPv6, IPv4 з портом (`IPv4:Port`) або IPv6 адреси з портом (`[IPv6]:Port`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
