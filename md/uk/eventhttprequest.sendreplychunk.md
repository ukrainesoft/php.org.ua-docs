Відправляє блок даних як частину поточної фрагментованої відповіді

-   [« EventHttpRequest::sendReply](eventhttprequest.sendreply.md)
    
-   [EventHttpRequest::sendReplyEnd »](eventhttprequest.sendreplyend.md)
    
-   [PHP Manual](index.md)
    
-   [EventHttpRequest](class.eventhttprequest.md)
    
-   Відправляє блок даних як частину поточної фрагментованої відповіді
    

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

-   [EventHttpRequest::sendReplyStart()](eventhttprequest.sendreplystart.md) - Ініціює фрагментарну відповідь
-   [EventHttpRequest::sendReplyEnd()](eventhttprequest.sendreplyend.md) - заповнює фрагментарну відповідь, звільняючи запит відповідним чином