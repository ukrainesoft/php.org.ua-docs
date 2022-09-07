---
navigation:
  - ffi.cdef.md: '« FFI::cdef'
  - ffi.isnull.md: 'FFI::isNull »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::free'
---
# FFI::free

(PHP 7> = 7.4.0, PHP 8)

FFI::free — Вивільняє некеровану структуру даних

### Опис

```methodsynopsis
public static FFI::free(FFI\CData &$ptr): void
```

Вивільняє створену раніше некеровану структуру даних.

### Список параметрів

`ptr`

Дескриптор некерованого покажчика структуру даних.

### Значення, що повертаються

Функція не повертає значення після виконання.
