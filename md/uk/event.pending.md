---
navigation:
  - event.getsupportedmethods.md: '« Event::getSupportedMethods'
  - event.set.md: 'Event::set »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::pending'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::pending

(PECL event >= 1.2.6-beta)

Event::pending — Перевірити, що подія перебуває в стані очікування або що вона запланована

### Опис

```methodsynopsis
public
   Event::pending(
    int
     $flags
   ): bool
```

Перевіряє, що подія перебуває у стані очікування або що вона запланована.

### Список параметрів

`flags`

Одна, або кілька констант, об'єднаних логічним АБО: **`Event::READ`** **`Event::WRITE`** **`Event::TIMEOUT`** **`Event::SIGNAL`**

### Значення, що повертаються

Повертає **`true`**, якщо подія запланована, або перебуває у стані очікування та **`false`**, якщо ні.
