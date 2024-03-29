---
navigation:
  - eventlistener.getbase.md: '« EventListener::getBase'
  - eventlistener.setcallback.md: 'EventListener::setCallback »'
  - index.md: PHP Manual
  - class.eventlistener.md: EventListener
title: 'EventListener::getSocketName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventListener::getSocketName

(PECL event >= 1.5.0)

EventListener::getSocketName — Отримує поточну адресу, до якої прив'язаний сокет слухача

### Опис

```methodsynopsis
public
   static
   EventListener::getSocketName(
    string
     &$address
   , 
    mixed
     &$port
    = ?): bool
```

Отримує адресу, до якої прив'язаний сокет слухача.

### Список параметрів

`address`

Вихідний параметр. IP-адреса залежно від сімейства адрес сокетів.

`port`

Вихідний параметр. Порт, якого прив'язаний сокет.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
