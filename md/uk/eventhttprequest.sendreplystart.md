---
navigation:
  - eventhttprequest.sendreplyend.md: '« EventHttpRequest::sendReplyEnd'
  - class.eventlistener.md: EventListener »
  - index.md: PHP Manual
  - class.eventhttprequest.md: EventHttpRequest
title: 'EventHttpRequest::sendReplyStart'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventHttpRequest::sendReplyStart

(PECL event >= 1.4.0-beta)

EventHttpRequest::sendReplyStart — Ініціює фрагментарну відповідь

### Опис

```methodsynopsis
public
   EventHttpRequest::sendReplyStart(
    int
     $code
   , 
    string
     $reason
   ): void
```

Ініціює відповідь, яку використовує `Transfer-Encoding` `chunked`

Це дозволяє стороні передавати відповідь назад клієнту. Це буде корисно, коли не всі дані відповіді доступні відразу, або при надсиланні дуже великих відповідей.

Викликаюча сторона повинна надати фрагменти даних за допомогою [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.md) і завершити відповідь, викликавши [EventHttpRequest::sendReplyEnd()](eventhttprequest.sendreplyend.md)

### Список параметрів

`code`

Код відповіді HTTP для надсилання.

`reason`

Коротке повідомлення, щоб надіслати код відповіді.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventHttpRequest::sendReplyChunk()](eventhttprequest.sendreplychunk.md) \- Відправляє блок даних, як частина поточної фрагментованої відповіді
-   [EventHttpRequest::sendReplyEnd()](eventhttprequest.sendreplyend.md) \- заповнює фрагментарну відповідь, звільняючи запит відповідним чином
