---
navigation:
  - eventdnsbase.setoption.md: '« EventDnsBase::setOption'
  - class.eventhttp.md: EventHttp »
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::setSearchNdots'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventDnsBase::setSearchNdots

(PECL event >= 1.2.6-beta)

EventDnsBase::setSearchNdots — Встановлює параметр 'ndots' для пошуку

### Опис

```methodsynopsis
public
   EventDnsBase::setSearchNdots(
    int
     $ndots
   ): bool
```

Устанавливает параметр\*\*`'ndots'`\*\* для пошуку. Встановлює кількість точок, що при знаходженні імені приводить до того, що перший запит не має пошукового домену.

### Список параметрів

`ndots`

Кількість точок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
