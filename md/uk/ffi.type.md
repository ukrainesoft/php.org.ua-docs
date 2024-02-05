---
navigation:
  - ffi.string.md: '« FFI::string'
  - ffi.typeof.md: 'FFI::typeof »'
  - index.md: PHP Manual
  - class.ffi.md: FFI
title: 'FFI::type'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# FFI::type

(PHP 7 >= 7.4.0, PHP 8)

FFI::type — Створює об'єкт FFI\\CType із декларації С

### Опис

```methodsynopsis
public static FFI::type(string $type): ?FFI\CType
```

```methodsynopsis
public FFI::type(string $type): ?FFI\CType
```

Функція створює та повертає об'єкт [FFI\\CType](class.ffi-ctype.md) для заданого рядка, що містить декларацію типу С. Якщо метод викликається статично, можна використовувати лише визначені імена типів С (наприклад, `int` `char`, і т.д.); якщо метод викликається як метод об'єкта, то допустимі будь-які певні йому типи.

### Список параметрів

`type`

Коректна декларація типу C як рядок (string).

### Значення, що повертаються

Повертає новий об'єкт [FFI\\CType](class.ffi-ctype.md)или\*\*`null`\*\*в случае возникновения ошибки.
