---
navigation:
  - eventhttprequest.sendreply.md: '« EventHttpRequest::sendReply'
  - eventhttprequest.sendreplyend.md: 'EventHttpRequest::sendReplyEnd »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::sendReplyChunk'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::sendReplyChunk

(PECL event >= 1.4.0-beta)

EventHttpRequest::sendReplyChunk — Відправляє блок даних як частину поточної фрагментованої відповіді

### Опис

```methodsynopsis
public
   EventHttpRequest::sendReplyChunk(
    EventBuffer
     $buf
   ): void
```

Відправляє блок даних як частину поточної фрагментованої відповіді. Після виклику цього методу, параметр `buf` буде порожнім.

### Список параметрів

`buf`

Фрагмент даних для надсилання, як частина відповіді.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventHttpRequest::sendReplyStart()](eventhttprequest.sendreplystart.md) \- Ініціює фрагментарну відповідь
-   [EventHttpRequest::sendReplyEnd()](eventhttprequest.sendreplyend.md) \- заповнює фрагментарну відповідь, звільняючи запит відповідним чином
