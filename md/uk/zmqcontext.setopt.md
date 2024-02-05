---
navigation:
  - zmqcontext.ispersistent.md: '« ZMQContext::isPersistent'
  - class.zmqsocket.md: ZMQSocket »
  - index.md: PHP Manual
  - class.zmqcontext.md: ZMQContext
title: 'ZMQContext::setOpt'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQContext::setOpt

(PECL zmq >= 1.0.4)

ZMQContext::setOpt — Встановити опцію сокету

### Опис

```methodsynopsis
public ZMQContext::setOpt(int $key, mixed $value): ZMQContext
```

Устанавливает опцию контекста ZMQ. Тип`value`зависит от`key`Смотрите[Типи Констант ZMQ](class.zmq.md#zmq.constants)

### Список параметрів

`key`

Одна из констант\*\*`ZMQ::CTXOPT_*`\*\*

`value`

Значення параметра.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQContextException.
