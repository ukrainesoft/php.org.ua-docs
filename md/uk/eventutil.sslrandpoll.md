---
navigation:
  - eventutil.setsocketoption.md: '« EventUtil::setSocketOption'
  - class.eventexception.md: EventException »
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::sslRandPoll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventUtil::sslRandPoll

(PECL event >= 1.2.6-beta)

EventUtil::sslRandPoll — Згенерувати ентропію за допомогою RAND\_poll() із OpenSSL

### Опис

```methodsynopsis
public
   static
   EventUtil::sslRandPoll(): void
```

Генерує ентропію за допомогою `RAND_poll()`из OpenSSL. (смотрите соответствующую документацию).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
