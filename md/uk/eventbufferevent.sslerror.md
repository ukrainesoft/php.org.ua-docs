---
navigation:
  - eventbufferevent.setwatermark.md: '« EventBufferEvent::setWatermark'
  - eventbufferevent.sslfilter.md: 'EventBufferEvent::sslFilter »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslError'
---
# EventBufferEvent::sslError

(PECL event >= 1.2.6-beta)

EventBufferEvent::sslError — Повертає останню помилку OpenSSL, повідомлену буферною подією

### Опис

```methodsynopsis
public
   EventBufferEvent::sslError(): string
```

Повертає останню помилку OpenSSL, повідомлену буферною подією.

> **Зауваження**
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок помилки OpenSSL, про яку повідомлялося в буферній події, або \*\*`false`\*\*якщо більше немає помилок для повернення.

### Приклади

**Приклад #1 Приклад використання **EventBufferEvent::sslError()****

```php
<?php
// Эта callbac-функция вызывается, когда какое-либо событие происходит в приёмнике событий,
// например, соединение закрыто или произошла ошибка
function ssl_event_cb($bev, $events, $ctx) {
    if ($events & EventBufferEvent::ERROR) {
        // Извлекаем ошибки из стека ошибок SSL
        while ($err = $bev->sslError()) {
            fprintf(STDERR, "Bufferevent error %s.\n", $err);
        }
    }

    if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
        $bev->free();
    }
}
?>
```

### Дивіться також

-   [EventBufferEvent::sslRenegotiate()](eventbufferevent.sslrenegotiate.md) - Повідомляє буферну подію розпочати перегляд SSL
