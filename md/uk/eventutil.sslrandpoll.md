---
navigation:
  - eventutil.setsocketoption.md: '« EventUtil::setSocketOption'
  - book.ftp.md: FTP »
  - index.md: PHP Manual
  - class.eventutil.md: EventUtil
title: 'EventUtil::sslRandPoll'
---
# EventUtil::sslRandPoll

(PECL event >= 1.2.6-beta)

EventUtil::sslRandPoll — Згенерувати ентропію за допомогою RANDpoll() із OpenSSL

### Опис

```methodsynopsis
public
   static
   EventUtil::sslRandPoll(): void
```

Генерує ентропію за допомогою `RAND_poll()` із OpenSSL. (Дивіться відповідну документацію).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.
