---
navigation:
  - class.sessionhandlerinterface.md: « SessionHandlerInterface
  - sessionhandlerinterface.destroy.md: 'SessionHandlerInterface::destroy »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::close

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::close — Закриває сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::close(): bool
```

Закриває поточну сесію. Ця функція автоматично виконується під час закриття сесії або явно через [session\_write\_close()](function.session-write-close.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
