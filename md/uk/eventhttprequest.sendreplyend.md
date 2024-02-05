---
navigation:
  - eventhttprequest.sendreplychunk.md: '« EventHttpRequest::sendReplyChunk'
  - eventhttprequest.sendreplystart.md: 'EventHttpRequest::sendReplyStart »'
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::sendReplyEnd'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [EventHttpRequest::sendReplyStart()](eventhttprequest.sendreplystart.md) \- Ініціює фрагментарну відповідь
-   [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.md) \- Відправляє блок даних, як частина поточної фрагментованої відповіді
