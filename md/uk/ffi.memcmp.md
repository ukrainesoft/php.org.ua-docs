---
navigation:
  - ffi.load.md: '« FFI::load'
  - ffi.memcpy.md: 'FFI::memcpy »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::memcmp'
---
# FFI::memcmp

(PHP 7> = 7.4.0, PHP 8)

FFI::memcmp — Порівнює дві області пам'яті

### Опис

```methodsynopsis
public static FFI::memcmp(string|FFI\CData &$ptr1, string|FFI\CData &$ptr2, int $size): int
```

Порівнює `size` байт пам'яті за вказівниками `ptr1` і `ptr2`. І `ptr1` і `ptr2` можуть бути будь-якими нативними структурами даних ([FFICData](class.ffi-cdata.md)), або рядками PHP.

### Список параметрів

`ptr1`

Вказівник на першу область пам'яті.

`ptr2`

Вказівник на другу область пам'яті.

`size`

Кількість байт для порівняння.

### Значення, що повертаються

Повертає < `0`, якщо вміст пам'яті для `ptr1` менше, ніж для `ptr2`, > `0`, якщо перше більше за друге і `0`якщо рівні.
