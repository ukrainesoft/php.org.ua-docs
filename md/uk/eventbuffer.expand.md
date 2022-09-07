---
navigation:
  - eventbuffer.enablelocking.md: '« EventBuffer::enableLocking'
  - eventbuffer.freeze.md: 'EventBuffer::freeze »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::expand'
---
# EventBuffer::expand

(PECL event >= 1.2.6-beta)

EventBuffer::expand — Резервує простір у буфері

### Опис

```methodsynopsis
public
   EventBuffer::expand(
    int
     $len
   ): bool
```

Змінює останній фрагмент пам'яті в буфері або додає новий фрагмент, щоб буфер був досить великий для змісту `len` байтів без додаткових виділень.

### Список параметрів

`len`

Кількість байтів, що резервуються для буфера

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
