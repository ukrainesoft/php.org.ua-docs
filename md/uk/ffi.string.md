---
navigation:
  - ffi.sizeof.md: '« FFI::sizeof'
  - ffi.type.md: 'FFI::type »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::string'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::string

(PHP 7 >= 7.4.0, PHP 8)

FFI::string — Створює рядок PHP з пам'яті

### Опис

```methodsynopsis
public static FFI::string(FFI\CData &$ptr, ?int $size = null): string
```

Створює змінну PHP типу string з `size`байт памяти, начиная с адреса по указателю`ptr`

### Список параметрів

`ptr`

Початок ділянки пам'яті, з якої буде створюватись рядок.

`size`

Кількість байт для копіювання в рядок. Якщо параметр `size`не задан или\*\*`null`\*\*, то`ptr` повинен вказувати на масив типу C `char`, що завершується нульовим байтом

### Значення, що повертаються

Рядок PHP.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `size` тепер припускає значення null; раніше значенням за умовчанням був |
