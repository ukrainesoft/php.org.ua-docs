---
navigation:
  - class.eventdnsbase.md: « EventDnsBase
  - eventdnsbase.addsearch.md: 'EventDnsBase::addSearch »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::addNameserverIp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Додає сервер імен до бази evdns\_base.

### Список параметрів

`ip`

Рядок сервера імен у вигляді адреси IPv4, IPv6, IPv4 з портом (`IPv4:Port`) або IPv6 адреси з портом (`[IPv6]:Port`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
