---
navigation:
  - ffi.alignof.md: '« FFI::alignof'
  - ffi.cast.md: 'FFI::cast »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::arrayType'
---
# FFI::arrayType

(PHP 7> = 7.4.0, PHP 8)

FFI::arrayType — Динамічно конструює новий тип масиву

### Опис

```methodsynopsis
public static FFI::arrayType(FFI\CType $type, array $dimensions): FFI\CType
```

Динамічно конструює новий тип масиву З елементами типу `type` та розмірностями, заданими в `dimensions`. У наступному прикладі `$t1` і `$t2` визначають масиви однакового типу:

```php
<?php
$t1 = FFI::type("int[2][3]");
$t2 = FFI::arrayType(FFI::type("int"), [2, 3]);
?>
```

### Список параметрів

`type`

Коректна декларація типу С, наприклад string, або заздалегідь створений об'єкт класу [FFICType](class.ffi-ctype.md)

`dimensions`

Масив, що визначає розмірність типу.

### Значення, що повертаються

Повертає новий об'єкт [FFICType](class.ffi-ctype.md)
