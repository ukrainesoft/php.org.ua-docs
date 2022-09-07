---
navigation:
  - eventhttpconnection.setmaxheaderssize.md: '« EventHttpConnection::setMaxHeadersSize'
  - eventhttpconnection.settimeout.md: 'EventHttpConnection::setTimeout »'
  - index.md: PHP Manual
  - class.eventhttpconnection.md: EventHttpConnection
title: 'EventHttpConnection::setRetries'
---
# EventHttpConnection::setRetries

(PECL event >= 1.2.6-beta)

EventHttpConnection::setRetries — Встановлює максимальну кількість повторів для з'єднання.

### Опис

```methodsynopsis
public
   EventHttpConnection::setRetries(
    int
     $retries
   ): void
```

Встановлює максимальну кількість повторів для з'єднання

### Список параметрів

`retries`

Кількість повторів . **`-1`** означає нескінченну кількість.

### Значення, що повертаються

Функція не повертає значення після виконання.
