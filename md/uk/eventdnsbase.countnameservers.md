---
navigation:
  - eventdnsbase.construct.md: '« EventDnsBase::\_\_construct'
  - eventdnsbase.loadhosts.md: 'EventDnsBase::loadHosts »'
  - index.md: PHP Manual
  - class.eventdnsbase.md: EventDnsBase
title: 'EventDnsBase::countNameservers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventDnsBase::countNameservers

(PECL event >= 1.2.6-beta)

EventDnsBase::countNameservers — Отримує кількість налаштованих серверів імен

### Опис

```methodsynopsis
public
   EventDnsBase::countNameservers(): int
```

Отримує кількість налаштованих серверів імен

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість налаштованих серверів імен (необов'язково запущених серверів імен). Це можна використовувати для додаткової перевірки того, були успішними виклики різних функцій конфігурації сервера імен.
