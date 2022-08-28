Створює об'єкт FFICType із декларації С

-   [« FFI::string](ffi.string.html)
    
-   [FFI::typeof »](ffi.typeof.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Створює об'єкт FFICType із декларації С
    

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

Функція створює та повертає об'єкт [FFI\\CType](class.ffi-ctype.html) для заданого рядка, що містить декларацію типу С. Якщо метод викликається статично, можна використовувати лише визначені імена типів С (наприклад, `int` `char`, і т.д.); якщо метод викликається як метод об'єкта, то допустимі будь-які певні йому типи.

### Список параметрів

`type`

Коректна декларація типу С чи об'єкт класу [FFI\\CType](class.ffi-ctype.html)

### Значення, що повертаються

Повертає новий об'єкт [FFI\\CType](class.ffi-ctype.html) або **`null`** у разі виникнення помилки.