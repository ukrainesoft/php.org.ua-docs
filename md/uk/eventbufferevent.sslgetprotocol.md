---
navigation:
  - eventbufferevent.sslgetcipherversion.md: '« EventBufferEvent::sslGetCipherVersion'
  - eventbufferevent.sslrenegotiate.md: 'EventBufferEvent::sslRenegotiate »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslGetProtocol'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::sslGetProtocol

(PECL event >= 1.10.0)

EventBufferEvent::sslGetProtocol — Повертає ім'я протоколу, який використовується для поточного з'єднання SSL

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetProtocol(): string
```

Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.

> **Зауваження** :
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.
