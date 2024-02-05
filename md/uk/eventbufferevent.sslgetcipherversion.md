---
navigation:
  - eventbufferevent.sslgetciphername.md: '« EventBufferEvent::sslGetCipherName'
  - eventbufferevent.sslgetprotocol.md: 'EventBufferEvent::sslGetProtocol »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslGetCipherVersion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::sslGetCipherVersion

(PECL event >= 1.10.0)

EventBufferEvent::sslGetCipherVersion — Повертає версію шифру, що використовується поточним SSL-з'єднанням

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetCipherVersion(): string
```

Отримує версію шифру, який використовується поточним з'єднанням SSL.

> **Зауваження** :
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточну версію шифрованого з'єднання SSL або \*\*`false`\*\*в случае возникновения ошибки.
