---
navigation:
  - eventhttprequest.free.md: '« EventHttpRequest::free'
  - eventhttprequest.getcommand.md: 'EventHttpRequest::getCommand »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::getBufferEvent'
---
# EventHttpRequest::getBufferEvent

(PECL event >= 1.8.0)

EventHttpRequest::getBufferEvent — Повертає об'єкт EventBufferEvent

### Опис

```methodsynopsis
public
   EventHttpRequest::closeConnection(): EventBufferEvent
```

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.md)представляє буферну подію, яка використовує з'єднання.

**Увага**

Лічильник посилань об'єкта, що повертається, буде збільшений на одиницю для захисту внутрішніх структур від передчасного руйнування при виклику методу з callback-функції користувача. Таким чином, об'єкт [EventBufferEvent](class.eventbufferevent.md) має бути явно звільнений за допомогою методу [EventBufferEvent::free()](eventbufferevent.free.md). В іншому випадку буде витік пам'яті.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.md)

### Дивіться також

-   [EventHttpRequest::getConnection()](eventhttprequest.getconnection.md) - Повертає об'єкт EventHttpConnection
