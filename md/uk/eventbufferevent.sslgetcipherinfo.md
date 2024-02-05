---
navigation:
  - eventbufferevent.sslfilter.md: '« EventBufferEvent::sslFilter'
  - eventbufferevent.sslgetciphername.md: 'EventBufferEvent::sslGetCipherName »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslGetCipherInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::sslGetCipherInfo

(PECL event >= 1.10.0)

EventBufferEvent::sslGetCipherInfo — Повертає текстовий опис шифру

### Опис

```methodsynopsis
public
   EventBufferEvent::sslGetCipherInfo(): string
```

Отримує опис поточного шифру за допомогою SSL API `SSL_CIPHER_description`(смотрите справочную страницу*SSL\_CIPHER\_get\_name(3)*

> **Зауваження** :
> 
> Функція доступна, лише якщо `Event` скомпільований за допомогою OpenSSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає текстовий опис шифру у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
