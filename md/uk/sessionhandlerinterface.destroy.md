---
navigation:
  - sessionhandlerinterface.close.md: '« SessionHandlerInterface::close'
  - sessionhandlerinterface.gc.md: 'SessionHandlerInterface::gc »'
  - index.md: PHP Manual
  - class.sessionhandlerinterface.md: SessionHandlerInterface
title: 'SessionHandlerInterface::destroy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SessionHandlerInterface::destroy

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::destroy(string $id): bool
```

Знищує сесію. Викликається функціями [session\_regenerate\_id()](function.session-regenerate-id.md)(с $destroy =**`true`** [session\_destroy()](function.session-destroy.md) та при невдалому завершенні функції [session\_decode()](function.session-decode.md)

### Список параметрів

`id`

Ідентифікатор сесії знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.
