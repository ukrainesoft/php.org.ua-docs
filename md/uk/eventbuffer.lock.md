---
navigation:
  - eventbuffer.freeze.md: '« EventBuffer::freeze'
  - eventbuffer.prepend.md: 'EventBuffer::prepend »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::lock'
---
# EventBuffer::lock

(PECL event >= 1.2.6-beta)

EventBuffer::lock — Отримує блокування буфера

### Опис

```methodsynopsis
public
   EventBuffer::lock(): void
```

Отримує блокування буфера. Може використовуватися в парі з [EventBuffer::unlock()](eventbuffer.unlock.md)щоб зробити набір операцій атомарним, тобто потокобезпечним. Зверніть увагу, що немає необхідності блокувати буфери для *окремих* операцій. Коли блокування увімкнено (дивіться [EventBuffer::enableLocking()](eventbuffer.enablelocking.md)), окремі операції над буферами подій є атомарними.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBuffer::unlock()](eventbuffer.unlock.md) - Знімає блокування, встановлене EventBuffer::lock
