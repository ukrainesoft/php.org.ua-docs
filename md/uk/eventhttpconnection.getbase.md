---
navigation:
  - eventhttpconnection.construct.md: '« EventHttpConnection::\_\_construct'
  - eventhttpconnection.getpeer.md: 'EventHttpConnection::getPeer »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::getBase'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpConnection::getBase

(PECL event >= 1.2.6-beta)

EventHttpConnection::getBase — Повертає базу подій, пов'язану зі з'єднанням

### Опис

```methodsynopsis
public
   EventHttpConnection::getBase(): EventBase
```

Повертає основу подій, пов'язану зі з'єднанням.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт [EventBase](class.eventbase.md), пов'язаний із з'єднанням. В іншому випадку - **`false`**
