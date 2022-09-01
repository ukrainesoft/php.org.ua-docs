---
navigation:
  - zmqcontext.getsocket.html: '« ZMQContext::getSocket'
  - zmqcontext.setopt.html: 'ZMQContext::setOpt »'
  - index.html: PHP Manual
  - class.zmqcontext.html: ZMQContext
title: 'ZMQContext::isPersistent'
---
# ZMQContext::isPersistent

(PECL zmq >= 0.5.0)

ZMQContext::isPersistent — Чи є контекст постійним

### Опис

```methodsynopsis
public ZMQContext::isPersistent(): bool
```

Визначає, чи контекст є постійним. Постійний контекст потрібний для постійного з'єднання, оскільки кожен сокет виділяється з контексту.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо контекст постійний і **`false`**, якщо ні.
