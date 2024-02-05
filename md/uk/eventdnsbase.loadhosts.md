---
navigation:
  - eventdnsbase.countnameservers.md: '« EventDnsBase::countNameservers'
  - eventdnsbase.parseresolvconf.md: 'EventDnsBase::parseResolvConf »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::loadHosts'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventDnsBase::loadHosts

(PECL event >= 1.2.6-beta)

EventDnsBase::loadHosts — Завантажує файл hosts (у тому ж форматі, що і /etc/hosts) з файлу hosts

### Опис

```methodsynopsis
public
   EventDnsBase::loadHosts(
    string
     $hosts
   ): bool
```

Завантажує файл hosts (у тому ж форматі, що й `/etc/hosts`) з файлу hosts.

### Список параметрів

`hosts`

Шлях до файлу хостів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
