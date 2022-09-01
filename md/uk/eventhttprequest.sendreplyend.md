---
navigation:
  - eventhttprequest.sendreplychunk.html: '« EventHttpRequest::sendReplyChunk'
  - eventhttprequest.sendreplystart.html: 'EventHttpRequest::sendReplyStart »'
  - index.html: PHP Manual
  - class.eventhttprequest.html: EventHttpRequest
title: 'EventHttpRequest::sendReplyEnd'
---
# EventHttpRequest::sendReplyEnd

(PECL event >= 1.4.0-beta)

EventHttpRequest::sendReplyEnd — Заповнює фрагментарну відповідь, звільняючи запит відповідним чином

### Опис

```methodsynopsis
public
   EventHttpRequest::sendReplyEnd(): void
```

Заповнює фрагментарну відповідь, звільняючи запит відповідним чином.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventHttpRequest::sendReplyStart()](eventhttprequest.sendreplystart.md) - Ініціює фрагментарну відповідь
-   [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.md) - Відправляє блок даних, як частина поточної фрагментованої відповіді
