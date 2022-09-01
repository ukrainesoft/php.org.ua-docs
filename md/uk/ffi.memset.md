---
navigation:
  - ffi.memcpy.html: '« FFI::memcpy'
  - ffi.new.html: 'FFI::new »'
  - index.html: PHP Manual
  - class.ffi.html: FFI
title: 'FFI::memset'
---
# FFI::memset

(PHP 7> = 7.4.0, PHP 8)

FFI::memset — Заповнити область пам'яті

### Опис

```methodsynopsis
public static FFI::memset(FFI\CData &$ptr, int $value, int $size): void
```

Заповнює `size` байт пам'яті за вказівником `ptr` значенням `value`

### Список параметрів

`ptr`

Вказівник початку ділянки пам'яті.

`value`

Значення заповнення.

`size`

Кількість байт, які будуть заповнені.

### Значення, що повертаються

Функція не повертає значення після виконання.
