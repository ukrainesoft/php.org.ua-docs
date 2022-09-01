---
navigation:
  - eventhttprequest.free.html: '« EventHttpRequest::free'
  - eventhttprequest.getcommand.html: 'EventHttpRequest::getCommand »'
  - index.html: PHP Manual
  - class.eventhttprequest.html: EventHttpRequest
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

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.html)представляє буферну подію, яка використовує з'єднання.

**Увага**

Лічильник посилань об'єкта, що повертається, буде збільшений на одиницю для захисту внутрішніх структур від передчасного руйнування при виклику методу з callback-функції користувача. Таким чином, об'єкт [EventBufferEvent](class.eventbufferevent.html) має бути явно звільнений за допомогою методу [EventBufferEvent::free()](eventbufferevent.free.html). В іншому випадку буде витік пам'яті.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.html)

### Дивіться також

-   [EventHttpRequest::getConnection()](eventhttprequest.getconnection.html) - Повертає об'єкт EventHttpConnection
