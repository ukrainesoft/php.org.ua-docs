Доступ до типів C

-   [« FFI\\CData](class.ffi-cdata.html)
    
-   [FFI\\CType::getAlignment »](ffi-ctype.getalignment.html)
    
-   [PHP Manual](index.html)
    
-   [FFI](book.ffi.html)
    
-   Доступ до типів C
    

# Доступ до типів C

(PHP 7> = 7.4.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class FFI\CType
     
     {

    /* Методы */
    
   public getAlignment(): int
public getArrayElementType(): FFI\CType
public getArrayLength(): int
public getAttributes(): int
public getEnumKind(): int
public getFuncABI(): int
public getFuncParameterCount(): int
public getFuncParameterType(int $index): FFI\CType
public getFuncReturnType(): FFI\CType
public getKind(): int
public getName(): string
public getPointerType(): FFI\CType
public getSize(): int
public getStructFieldNames(): array
public getStructFieldOffset(string $name): int
public getStructFieldType(string $name): FFI\CType

   }
```

## Зміст

-   [FFI\\CType::getAlignment](ffi-ctype.getalignment.html) - Опис
-   [FFI\\CType::getArrayElementType](ffi-ctype.getarrayelementtype.html) - Опис
-   [FFI\\CType::getArrayLength](ffi-ctype.getarraylength.html) - Опис
-   [FFI\\CType::getAttributes](ffi-ctype.getattributes.html) - Опис
-   [FFI\\CType::getEnumKind](ffi-ctype.getenumkind.html) - Опис
-   [FFI\\CType::getFuncABI](ffi-ctype.getfuncabi.html) - Опис
-   [FFI\\CType::getFuncParameterCount](ffi-ctype.getfuncparametercount.html) - Опис
-   [FFI\\CType::getFuncParameterType](ffi-ctype.getfuncparametertype.html) - Опис
-   [FFI\\CType::getFuncReturnType](ffi-ctype.getfuncreturntype.html) - Опис
-   [FFI\\CType::getKind](ffi-ctype.getkind.html) - Опис
-   [FFI\\CType::getName](ffi-ctype.getname.html) - Опис
-   [FFI\\CType::getPointerType](ffi-ctype.getpointertype.html) - Опис
-   [FFI\\CType::getSize](ffi-ctype.getsize.html) - Опис
-   [FFI\\CType::getStructFieldNames](ffi-ctype.getstructfieldnames.html) - Опис
-   [FFI\\CType::getStructFieldOffset](ffi-ctype.getstructfieldoffset.html) - Опис
-   [FFI\\CType::getStructFieldType](ffi-ctype.getstructfieldtype.html) - Опис