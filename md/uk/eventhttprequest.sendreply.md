---
navigation:
  - eventhttprequest.senderror.html: '« EventHttpRequest::sendError'
  - eventhttprequest.sendreplychunk.html: 'EventHttpRequest::sendReplyChunk »'
  - index.html: PHP Manual
  - class.eventhttprequest.html: EventHttpRequest
title: 'EventHttpRequest::sendReply'
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

-   [EventHttpRequest::sendError()](eventhttprequest.senderror.html) - Надсилає HTML-повідомлення про помилку клієнту
-   [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.html) - Відправляє блок даних, як частина поточної фрагментованої відповіді
