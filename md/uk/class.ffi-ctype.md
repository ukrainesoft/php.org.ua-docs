Доступ до типів C

-   [« FFICData](class.ffi-cdata.html)
    
-   [FFICType::getAlignment »](ffi-ctype.getalignment.html)
    
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

-   [FFICType::getAlignment](ffi-ctype.getalignment.html) - Опис
-   [FFICType::getArrayElementType](ffi-ctype.getarrayelementtype.html) - Опис
-   [FFICType::getArrayLength](ffi-ctype.getarraylength.html) - Опис
-   [FFICType::getAttributes](ffi-ctype.getattributes.html) - Опис
-   [FFICType::getEnumKind](ffi-ctype.getenumkind.html) - Опис
-   [FFICType::getFuncABI](ffi-ctype.getfuncabi.html) - Опис
-   [FFICType::getFuncParameterCount](ffi-ctype.getfuncparametercount.html) - Опис
-   [FFICType::getFuncParameterType](ffi-ctype.getfuncparametertype.html) - Опис
-   [FFICType::getFuncReturnType](ffi-ctype.getfuncreturntype.html) - Опис
-   [FFICType::getKind](ffi-ctype.getkind.html) - Опис
-   [FFICType::getName](ffi-ctype.getname.html) - Опис
-   [FFICType::getPointerType](ffi-ctype.getpointertype.html) - Опис
-   [FFICType::getSize](ffi-ctype.getsize.html) - Опис
-   [FFICType::getStructFieldNames](ffi-ctype.getstructfieldnames.html) - Опис
-   [FFICType::getStructFieldOffset](ffi-ctype.getstructfieldoffset.html) - Опис
-   [FFICType::getStructFieldType](ffi-ctype.getstructfieldtype.html) - Опис