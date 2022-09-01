---
navigation:
  - ffi.string.html: '« FFI::string'
  - ffi.typeof.html: 'FFI::typeof »'
  - index.html: PHP Manual
  - class.ffi.html: FFI
title: 'FFI::type'
---
# FFI::type

(PHP 7> = 7.4.0, PHP 8)

FFI::type — Створює об'єкт FFICType із декларації С

### Опис

```methodsynopsis
public static FFI::type(string $type): ?FFI\CType
```

```methodsynopsis
public FFI::type(string $type): ?FFI\CType
```

Функція створює та повертає об'єкт [FFICType](class.ffi-ctype.md) для заданого рядка, що містить декларацію типу С. Якщо метод викликається статично, можна використовувати лише визначені імена типів С (наприклад, `int` `char`, і т.д.); якщо метод викликається як метод об'єкта, то допустимі будь-які певні йому типи.

### Список параметрів

`type`

Коректна декларація типу С чи об'єкт класу [FFICType](class.ffi-ctype.md)

### Значення, що повертаються

Повертає новий об'єкт [FFICType](class.ffi-ctype.md) або **`null`** у разі виникнення помилки.
