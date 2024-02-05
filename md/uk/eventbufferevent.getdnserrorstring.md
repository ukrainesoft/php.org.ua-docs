---
navigation:
  - eventbufferevent.free.md: '« EventBufferEvent::free'
  - eventbufferevent.getenabled.md: 'EventBufferEvent::getEnabled »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::getDnsErrorString'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::getDnsErrorString

(PECL event >= 1.2.6-beta)

EventBufferEvent::getDnsErrorString — Повертає рядок, що описує останню невдалу спробу пошуку DNS

### Опис

```methodsynopsis
public
   EventBufferEvent::getDnsErrorString(): string
```

Повертає рядок, що описує останню невдалу спробу пошуку DNS, зроблену [EventBufferEvent::connectHost()](eventbufferevent.connecthost.md), або порожній рядок, якщо помилку DNS не виявлено.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, що описує помилку пошуку DNS або порожній рядок, якщо помилки не відбулося.

### Дивіться також

-   [EventBufferEvent::connectHost()](eventbufferevent.connecthost.md) \- Підключається на ім'я хоста з можливістю асинхронного дозволу DNS
