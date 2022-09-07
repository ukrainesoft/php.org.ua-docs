---
navigation:
  - eventbufferevent.sslgetprotocol.md: '« EventBufferEvent::sslGetProtocol'
  - eventbufferevent.sslsocket.md: 'EventBufferEvent::sslSocket »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'Event BufferEvent::ssl Renegotiate'
---
# Event BufferEvent::ssl Renegotiate

(PECL event >= 1.2.6-beta)

EventBufferEvent::sslRenegotiate — Повідомляє буферну подію розпочати перегляд SSL

### Опис

```methodsynopsis
public
   EventBufferEvent::sslRenegotiate(): void
```

Повідомляє про буферну подію розпочати перегляд SSL.

**Увага**

Виклик цієї функції перегляне SSL та викличе відповідні callback-функції буферної події. Це складна тема; це, як правило, слід уникати, якщо тільки ви дійсно знаєте, що робите, тим більше, що у багатьох версіях SSL були відомі проблеми безпеки, пов'язані з переглядом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
