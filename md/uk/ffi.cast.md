Здійснює перетворення типу C

-   [« FFI::arrayType](ffi.arraytype.html)
    
-   [FFI::cdef »](ffi.cdef.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Здійснює перетворення типу C
    

# FFI::cast

(PHP 7> = 7.4.0, PHP 8)

FFI::cast — Перетворює тип C

### Опис

```methodsynopsis
public static FFI::cast(FFI\CType|string $type, FFI\CData|int|float|bool|null &$ptr): ?FFI\CData
```

```methodsynopsis
public FFI::cast(FFI\CType|string $type, FFI\CData|int|float|bool|null &$ptr): ?FFI\CData
```

**FFI::cast()** створює новий об'єкт класу [FFICData](class.ffi-cdata.html)що вказує на ту саму структуру C, але асоційований з іншим типом. Отриманий об'єкт не стає власником даних, тому вихідний покажчик `ptr` повинен залишатися живим довше за отриманий об'єкт. Тип C повинен бути заданий як рядок, що містить ім'я будь-якого коректного типу, або як об'єкт [FFICType](class.ffi-ctype.html). Якщо метод викликається статично, можна використовувати лише визначені імена типів З (наприклад, `int` `char`, Etc.); якщо метод викликається як метод об'єкта, то допустимі будь-які певні йому типи.

### Список параметрів

`type`

Рядок з ім'ям типу С або об'єкт класу [FFICType](class.ffi-ctype.html)

`ptr`

Дескриптор покажчика структуру даних З.

### Значення, що повертаються

Повертає новий об'єкт [FFICData](class.ffi-cdata.html)