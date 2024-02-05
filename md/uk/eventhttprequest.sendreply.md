---
navigation:
  - eventhttprequest.senderror.md: '« EventHttpRequest::sendError'
  - eventhttprequest.sendreplychunk.md: 'EventHttpRequest::sendReplyChunk »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::sendReply'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::sendReply

(PECL event >= 1.4.0-beta)

EventHttpRequest::sendReply — Надсилає HTML-відповідь клієнту

### Опис

```methodsynopsis
public
   EventHttpRequest::sendReply(
    int
     $code
   , 
    string
     $reason
   , 
    EventBuffer
     $buf
    = ?): void
```

Відправляє HTML0відповідь клієнту. Тіло відповіді складається з даних у необов'язковому параметрі `buf`

### Список параметрів

`code`

Код відповіді HTTP для надсилання.

`reason`

Коротке повідомлення, щоб надіслати код відповіді.

`buf`

Тіло відповіді.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventHttpRequest::sendError()](eventhttprequest.senderror.md) \- Надсилає HTML-повідомлення про помилку клієнту
-   [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.md) \- Відправляє блок даних, як частина поточної фрагментованої відповіді
