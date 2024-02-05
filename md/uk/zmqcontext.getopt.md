---
navigation:
  - zmqcontext.construct.md: '« ZMQContext::\_\_construct'
  - zmqcontext.getsocket.md: 'ZMQContext::getSocket »'
  - index.md: PHP Manual
  - class.zmqcontext.md: ZMQContext
title: 'ZMQContext::getOpt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQContext::getOpt

(PECL zmq >= 1.0.4)

ZMQContext::getOpt — Отримати опцію контексту

### Опис

```methodsynopsis
public ZMQContext::getOpt(string $key): mixed
```

Повертає значення опції контексту.

### Список параметрів

`key`

Целое число, отражающее значение опции. Смотрите описание констант\*\*`ZMQ::CTXOPT_*`\*\*

### Значення, що повертаються

Повертає string або int залежно від `key`. У разі помилки викидає виняток ZMQContextException.
