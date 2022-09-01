---
navigation:
  - class.ffi.html: « FFI
  - ffi.alignof.html: 'FFI::alignof »'
  - index.html: PHP Manual
  - class.ffi.html: FFI
title: 'FFI::addr'
---
# FFI::addr

(PHP 7> = 7.4.0, PHP 8)

FFI::addr — Створює некерований покажчик даних C

### Опис

```methodsynopsis
public static FFI::addr(FFI\CData &$ptr): FFI\CData
```

Створює некерований покажчик даних C, представлені заданим [FFICData](class.ffi-cdata.md). Початковий `ptr` повинен пережити результуючий покажчик. Ця функція використовується головним чином передачі аргументів в функцію C за покажчиком.

### Список параметрів

`ptr`

Дескриптор некерованого покажчика структуру даних.

### Значення, що повертаються

Повертає новий об'єкт [FFICData](class.ffi-cdata.md)
