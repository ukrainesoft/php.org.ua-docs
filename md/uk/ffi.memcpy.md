---
navigation:
  - ffi.memcmp.md: '« FFI::memcmp'
  - ffi.memset.md: 'FFI::memset »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::memcpy'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::memcpy

(PHP 7 >= 7.4.0, PHP 8)

FFI::memcpy — Копіює вміст однієї області пам'яті в іншу

### Опис

```methodsynopsis
public static FFI::memcpy(FFI\CData &$to, FFI\CData|string &$from, int $size): void
```

Копіює `size`байт из области памяти`from`в область памяти`to`

### Список параметрів

`to`

Цільова область пам'яті.

`from`

Область пам'яті, звідки відбуватиметься копіювання.

`size`

Кількість байт для копіювання.

### Значення, що повертаються

Функція не повертає значення після виконання.
