---
navigation:
  - sessionhandlerinterface.close.md: '« SessionHandlerInterface::close'
  - sessionhandlerinterface.gc.md: 'SessionHandlerInterface::gc »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::destroy'
---
# SessionHandlerInterface::destroy

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::destroy(string $id): bool
```

Знищує сесію. Викликається функціями [sessionregenerateid()](function.session-regenerate-id.md) (З $destroy = **`true`** [sessiondestroy()](function.session-destroy.md) та при невдалому завершенні функції [sessiondecode()](function.session-decode.md)

### Список параметрів

`id`

Ідентифікатор сесії знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
