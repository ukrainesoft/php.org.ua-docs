---
navigation:
  - eventbufferevent.sslgetprotocol.md: '« EventBufferEvent::sslGetProtocol'
  - eventbufferevent.sslsocket.md: 'EventBufferEvent::sslSocket »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslRenegotiate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::sslRenegotiate

(PECL event >= 1.2.6-beta)

EventBufferEvent::sslRenegotiate — Повідомляє буферну подію розпочати перегляд SSL

### Опис

```methodsynopsis
public
   EventBufferEvent::sslRenegotiate(): void
```

Повідомляє про буферну подію розпочати перегляд SSL.

**Увага**

Виклик цієї функції перегляне SSL та викличе відповідні callback-функції буферної події. Це складна тема; Це, як правило, слід уникати, якщо тільки ви дійсно знаєте, що робите, тим більше, що у багатьох версіях SSL були відомі проблеми безпеки, пов'язані з переглядом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
