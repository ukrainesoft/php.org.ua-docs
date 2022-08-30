Динамічно конструює новий тип масиву

-   [« FFI::alignof](ffi.alignof.html)
    
-   [FFI::cast »](ffi.cast.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](class.ffi.html)
    
-   Динамічно конструює новий тип масиву
    

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

Коректна декларація типу С, наприклад string, або заздалегідь створений об'єкт класу [FFICType](class.ffi-ctype.html)

`dimensions`

Масив, що визначає розмірність типу.

### Значення, що повертаються

Повертає новий об'єкт [FFICType](class.ffi-ctype.html)