---
navigation:
  - class.ffi.md: « FFI
  - ffi.alignof.md: 'FFI::alignof »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::addr'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::addr

(PHP 7 >= 7.4.0, PHP 8)

FFI::addr — Створює некерований покажчик даних C

### Опис

```methodsynopsis
public static FFI::addr(FFI\CData &$ptr): FFI\CData
```

Створює некерований покажчик даних C, представлені заданим [FFI\\CData](class.ffi-cdata.md). Початковий `ptr` повинен пережити результуючий покажчик. Ця функція використовується головним чином передачі аргументів у функцію C за покажчиком.

### Список параметрів

`ptr`

Дескриптор некерованого покажчика структуру даних.

### Значення, що повертаються

Повертає новий об'єкт [FFI\\CData](class.ffi-cdata.md)
