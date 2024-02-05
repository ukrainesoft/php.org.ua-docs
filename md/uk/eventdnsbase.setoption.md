---
navigation:
  - eventdnsbase.parseresolvconf.md: '« EventDnsBase::parseResolvConf'
  - eventdnsbase.setsearchndots.md: 'EventDnsBase::setSearchNdots »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::setOption'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventDnsBase::setOption

(PECL event >= 1.2.6-beta)

EventDnsBase::setOption — Встановлює параметр конфігурації

### Опис

```methodsynopsis
public
   EventDnsBase::setOption(
    string
     $option
   , 
    string
     $value
   ): bool
```

Встановлює параметр конфігурації.

### Список параметрів

`option`

В даний час доступні такі параметри конфігурації: `"ndots"` `"timeout"` `"max-timeouts"` `"max-inflight"`и`"attempts"`

`value`

Значення параметра.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
