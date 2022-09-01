---
navigation:
  - eventbufferevent.sslgetcipherinfo.md: '« EventBufferEvent::sslGetCipherInfo'
  - eventbufferevent.sslgetcipherversion.md: 'EventBufferEvent::sslGetCipherVersion »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslGetCipherName'
---
# EventBufferEvent::sslGetCipherName

(PECL event >= 1.10.0)

EventBufferEvent::sslGetCipherName — Повертає поточне ім'я шифру з'єднання SSL

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetCipherName(): string
```

Отримує ім'я шифру, який використовується поточним з'єднанням SSL.

> **Зауваження**
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточне ім'я шифру SSL-з'єднання або **`false`** у разі виникнення помилки.
